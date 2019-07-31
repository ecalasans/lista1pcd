##Lista 1

####Ex 1.3.
Para um número de cores = $2^{n}$, onde $n \in \N$:
~~~
n_cores = 2^n
core_difference = 1
divisor = 2
k = 0

enquanto divisor <= n_cores{
    //Tipo de core:  envia soma(E) ou recebe e soma(R)
    char tipo_core[n_cores]

    //Pares de cores
    int pares_cores[n_cores/2][2]

    //Percorre os cores e os classifica em E ou R
    para(i = 0; i < n_cores; i++){
        //Se for divisível por divisor é E;  se não, é R
        se(i % divisor == 0){
            tipo_core[i] = "R"
        } senão {
            tipo_core[i] = "E"
        }
    }

    //Após preencher tipo_core preenche a matriz de pares_cores
    para(j = 0; j < n_cores; j++){
        //Verifica a relação entre 2 cores e core_difference e
        faz o pareamento
        se(j + core_difference = (j + 1)) e ((j+1) - core_difference == j){
            pares_cores[k][j] = j
            pares_cores[k][j+1] = j + 1
            k++
        } senão {
            continua
        }
    }

}

~~~
