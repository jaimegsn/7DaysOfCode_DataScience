<h2>
Log Manual dos erros: (Com minhas explicações do que encontrei na internet e soluções)
</h2>

<h3>
1- 'utf-8' codec can't decode byte 0xf3 in position 213: invalid continuation byte :
</h3>
Explicação:<br> 
o Utf-8 não ta conseguindo ler um(s) valor do arquivo, 
<br>
Solução:<br>
achar o codec correto (no meu caso era latin-1).<br> 
Mudar o encoding na abertura do arquivo ex: pd.read_csv('arquivo', encoding='codec que irá solucionar'(utf-8,latin-1...))


<h3 style="color:blue">
2-Error tokenizing data. C error: Expected 1 fields in line 3, saw 3
</h3>
Explicação:<br>
Nesse caso o dataset tinha 3 colunas na 1° linha e nas linhas abaixo tinha >3 colunas e isso tava gerando uma irregularidade na leitura do arquivo, então usei o skiprows=[0], para desconsiderar essas 3 colunas iniciais, visto que eram dados desnecessários para uma Futura análise

