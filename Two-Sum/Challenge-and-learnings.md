# Two Sum (Fácil)
Dado um array de inteiros `nums` e um inteiro `target`, retorne os índices dos dois números cuja soma seja igual a `target`.

Você pode assumir que cada entrada terá exatamente uma solução e não pode usar o mesmo elemento duas vezes.

Você pode retornar a resposta em qualquer ordem.

### Exemplo 1:
- Input: nums = [2,7,11,15]
- target = 9
- Output: [0,1]

### Exemplo 2:
- Input: nums = [3,2,4]
- target = 6
- Output: [1,2]

## Solução
```
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int[] answer = new int[2];
        for (int i = 0; i < nums.length; i++){
            int control = 0;
            for(int j = 0; j < nums.length; j++){
                if(nums[i] + nums[j] == target && i != j){
                    answer[0] = i;
                    answer[1] = j;
                    control = 1;
                    break;
                }
            }
            if(control == 1){break;};
        }
        return answer;
    }
}
```

# Aprendizados

### Reforço da sintaxe do FOR

for (`Inicio da variável de controle`;`Condição para a variavel de controle`;`Incremento da variavel de controle`){}

```

for (int i = 0; i < 10; i++){}
```

### Vetores

Aprendi a Logica por traz dos Vetores em java.

Acontece que um Vetor em java é um objeto e portanto precisa ser instanciado previamente. O vetor pode ser de varios tipos também: int, double, String e por ai vai

```

int[] *nome do vetor* = new int[];
```

os "[]" representam o vetor.

Para incluir ou alterar valor no vetor passamos seu nome e o indice entre chaves. Lembrando que a contagem das posições começa em 0 (0,1,2,3,4,5....).

```

*nome do vetor*[2]
```