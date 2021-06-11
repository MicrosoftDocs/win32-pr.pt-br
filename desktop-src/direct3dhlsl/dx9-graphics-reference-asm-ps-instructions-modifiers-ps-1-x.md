---
title: Modificadores para ps_1_X
description: Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino. Saiba mais sobre modificadores para ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c97196040a8f5f9888cb2fb354dcc18ca3743c7
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988721"
---
# <a name="modifiers-for-ps_1_x"></a>Modificadores para PS \_ 1 \_ X

Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino. Por exemplo, use-os para multiplicar ou dividir o resultado por um fator de dois ou para fixe o resultado entre zero e um. Os modificadores de instrução são aplicados depois que a instrução é executada, mas antes de gravar o resultado no registro de destino.

Uma lista dos modificadores é mostrada abaixo.



| Modificador | Descrição                   | Syntax           | Versão |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |
| \_X2     | Multiplicar por 2                 | instrução \_ X2  | X       | X    | X    | X    |
| \_X4     | Multiplicar por 4                 | \_X4 instruções  | X       | X    | X    | X    |
| \_x8     | Multiplicar por 8                 | x8 de instruções \_  |         |      |      | X    |
| \_D2     | Dividir por 2                   | instrução \_ D2  | X       | X    | X    | X    |
| \_D4     | Dividir por 4                   | instrução \_ D4  |         |      |      | X    |
| \_D8     | Dividir por 8                   | instrução \_ D8  |         |      |      | X    |
| \_saturação    | Saturação (fixe de 0 e 1) | instrução \_ SAT | X       | X    | X    | X    |



 

-   O modificador de multiplicação multiplica os dados de registro por uma potência de dois após sua leitura. Isso é o mesmo que uma mudança à esquerda.
-   O modificador de divisão divide os dados de registro por uma potência de dois após sua leitura. Isso é o mesmo que uma mudança à direita.
-   O modificador saturação coloca o intervalo de valores de registro de zero para um.

Os modificadores de instrução podem ser usados em instruções aritméticas. Eles não podem ser usados em instruções de endereço de textura.

Modificador de multiplicação

Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e multiplica o resultado por dois.


```
add_x2 dest, src0, src1
```



Este exemplo combina dois modificadores de instrução. Primeiro, duas cores nos operandos de origem (src0 e src1) são adicionadas. Em seguida, o resultado é multiplicado por dois e clamped entre 0,0 e 1,0 para cada componente. O resultado é salvo no registro de destino.


```
add_x2_sat dest, src0, src1
```



Modificador de divisão

Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e divide o resultado por dois.


```
add_d2 dest, src0, src1
```



Modificador saturado

Para obter instruções aritméticas, o modificador de saturação coloca o resultado dessa instrução no intervalo de 0,0 a 1,0 para cada componente. O exemplo a seguir mostra como usar esse modificador de instrução.


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



Essa operação ocorre depois de qualquer modificador de instrução de multiplicação ou de divisão. \_SAT é usado com mais frequência para fixe pontos de produtos. No entanto, ele também habilita a emulação consistente de métodos de várias passagens, em que o buffer de quadro está sempre no intervalo de 0 a 1 e da sintaxe multitextura DirectX 6 e 7,0, na qual a saturação é definida para ocorrer em cada estágio.

Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e coloca o resultado no intervalo de 0,0 a 1,0 para cada componente.


```
add_sat dest, src0, src1
```



Este exemplo combina dois modificadores de instrução. Primeiro, duas cores nos operandos de origem (src0 e src1) são adicionadas. O resultado é multiplicado por dois e clamped entre 0,0 e 1,0 para cada componente. O resultado é salvo no registro de destino.


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




