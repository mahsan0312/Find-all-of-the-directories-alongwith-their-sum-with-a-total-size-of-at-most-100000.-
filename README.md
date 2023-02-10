# Find-all-of-the-directories-alongwith-their-sum-with-a-total-size-of-at-most-100000.-
Find all of the directories with a total size of at most 100000. What is the sum of the total sizes of those directories?

In Linux: 

Following command will find all of the directories with a total size of at most 100000. 
find . -type d -size -100000c -exec du -sh {} + | awk '{print $1}'

find . -type d -size -100000c -print


Following command will find the sum of the total sizes of those directories?
find . -type d -size -100000c -exec du -s {} + | awk '{sum+=$1} END {print sum}'

ls | ruby -ne 'BEGIN{a= []}; a <<  File.size($_.chomp).to_i; END{puts a.sum}'
The code above gets the file size of each file, puts it into an array, and prints the sum.

du -ach

ls -al

du -ch $file_list | tail -1 | cut -f 1


echo '1' > this

hexdump this

ls -l this
-rw-r--r-- 1 schwern staff 2 Dec  5 15:16 this

du -h this

du --apparent-size -h this

ruby -e 'puts File.size(ARGV[0])' this
