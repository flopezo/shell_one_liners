# shell_one_liners

Single lines of bash commands 

## Contents

- [find & grep](#find--grep)

Read lines, search for each line string, and find matching files with .ab1 extension

    while read line; do find . -type f -name "*.ab1" -exec grep -l "$line" /dev/null '{}' \+; done < ../voucher_id_list.txt
    while read line; do grep -l -r "$line" .; done < ../voucher_id_list.txt
    grep -l -f ../voucher_id_list.txt ./*
    
Read list and move files  

    cat list_of_files.txt | xargs mv -t /destination_folder/
  
