# Thales
#!/bin/bash

CALCULA_SALARIO() {
echo ""
read -p " Informe o salário: " sal
sal=$(sed 's/,/\./' <<< "$sal")
tx=$(awk '{if($1<=0) print "0";else if($1<=500) print "20";else if($1>500) print "10"}' <<< "$sal")
    if ((tx==0));then 
    exit
    else
    echo -e "\n O salário: $sal foi acrescido de ${tx}%\n Salário Corrigido: $(awk '{printf "%.2f" ,$1*($2/100+1)}' <<< "$sal $tx"|sed 's/\./,/')"
    CALCULA_SALARIO
    fi
}
tput clear
CALCULA_SALARIO
