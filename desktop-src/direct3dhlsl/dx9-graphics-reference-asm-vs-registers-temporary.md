---
title: Registro temporário (referência do HLSL VS)
description: Um registro temporário de sombreador de vértice é usado para manter resultados intermediários.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104293612"
---
# <a name="temporary-register-hlsl-vs-reference"></a>Registro temporário (referência do HLSL VS)

Um registro temporário de sombreador de vértice é usado para manter resultados intermediários.

Um registro temporário deve ser inicializado antes de ser usado. Cada registro temporário tem acesso de gravação única e de leitura tripla. Isso significa que uma única instrução de sombreador pode usar até três registros temporários como entradas.

Os valores em um registro temporário que permanecem de invocações anteriores do sombreador de vértice não podem ser usados.

Um registro consiste em propriedades que determinam se o registro se comporta.



| Propriedade        | Descrição                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name            | r \[ n \] . n é um número de registro opcional. O padrão é 0 e é o valor usado se nenhum valor for especificado.                                                                                 |
| Contagem           | Um máximo de 12 registros.                                                                                                                                                                  |
| Permissões de e/s | Leitura/gravação. Esse registro pode ser lido ou gravado pela API ou pelo sombreador.                                                                                                               |
| Portas de leitura      | O número de vezes que um registro pode ser lido em uma única instrução é 3. Um registro temporário é o único registro que pode ser lido e gravado mais de uma vez em uma única instrução. |



 

Cada registro temporário tem acesso de gravação única e de leitura tripla. Portanto, uma instrução pode ter até três registros temporários em seu conjunto de operandos de origem de entrada.

Nenhum valor em um registro temporário que permaneça de invocações precedentes do sombreador de vértice pode ser usado. Os sombreadores de vértice que lêem um valor de um registro temporário antes de gravar nele falharão na chamada à API do Direct3D para criar o sombreador de vértice.

## <a name="example"></a>Exemplo

Aqui está um exemplo usando um registro temporário:


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro temporário     | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




