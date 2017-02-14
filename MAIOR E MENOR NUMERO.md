#! bin/bash
# Autor: Daniel
# Criação 15/02/2017

clear 
echo "Qual eh seu Sexo?"
read Sexo
echo "Fale um numero"
read N01
echo "Digite outro numero"
read N02
echo "Digite Novamente Outro Numero"
read N03
clear


if (( $Sexo ="Homem" )); then
	if (( $N01 > $N02 )); then
		echo "O maior numero eh $N01"
	else
		echo "O maior numero eh $N02"
	fi
else
	if (( $N01 < $N02 )); then
		echo "O menor numero eh $N01"
	else
		echo " O menor numero eh $N02"
	fi

	if (( $N02 > $N03 )); then
		echo "O menor numero eh $N02"
	else
		echo " O maior numero eh $N03"
	fi
fi

