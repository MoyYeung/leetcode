        根据身高倒序排列，若遇到相同的h值，则将k值小的排在前面。
        Sort them by their h value in a descending way. If the h value are the same, put the one having smaller k value in the front.</span>
        实例化一个list，将k值作为索引，将值插入到list中
        Initialize a list, use k value as the index and insert element into the list.


#java:
        public int[][] solution(int[][] people){
            //array sort using comparator
            List<int[]> linkedList = new LinkedList<>();

            Arrays.sort(people, new Comparator<int[]>){
            int compare(int o1, int o2){
            return o1[0]!=o2[0]? -o1[0] + o2[0] :o1[0]-o2[0];
             }
            }

                for(int[] cur:people){
                    linkedList.add(cur[1],cur);
                }

            return linkedList.toArray(new int[people.lengh][]);
        }