---
title: Dimensionamento assinado do registro de origem
description: Subtrai 0,5 de cada canal e dimensiona o resultado por 2,0. O nome BX2 vem de tendência e escala – vezes-dois, que é a operação que ele executa.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160502"
---
# <a name="source-register-signed-scaling"></a>Dimensionamento assinado do registro de origem

Subtrai 0,5 de cada canal e dimensiona o resultado por 2,0. O nome BX2 vem de tendência e escala – vezes-dois, que é a operação que ele executa.

## <a name="syntax"></a>Syntax


```
source register_bx2
```



## <a name="register"></a>Registre-se

Registro de origem. Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentários

Essa operação é normalmente usada para expandir dados de \[ 0,0 para 1,0 \] para \[ -1,0 a 1,0 \] . Esse modificador foi projetado para uso com as instruções aritméticas. Esse modificador é normalmente usado em entradas para a instrução de produto dot ([DP3-PS](dp3---ps.md)). \_O uso de BX2 em dados fora do intervalo de 0 a 1 pode produzir resultados indefinidos.

A operação de dimensionamento assinado é aplicada aos dados lidos do registro antes da execução da próxima instrução. A operação é aplicada a todos os quatro canais de cores (RGBA) da seguinte maneira:


```
y = 2(x - 0.5)
```



O conteúdo do registro não é alterado. O modificador é aplicado somente aos dados lidos do registro.

Esse modificador é mutuamente exclusivo com o [registro de origem inverter](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) para que não possa ser aplicado ao mesmo registro.

Informações de versão:

-   Para \_ o PS 1 \_ 0 e \_ o PS 1 \_ 1, você pode usar \_ BX2 em qualquer registro de origem para obter instruções de textura do formulário texm3x2 \* e texm3x3 \* . \_BX2 não pode ser usado em nenhuma das outras instruções de textura, como [texreg2ar-PS](texreg2ar---ps.md) ou [texreg2gb-PS](texreg2gb---ps.md).
-   Para \_ o PS 1 \_ 2 e \_ o PS 1 \_ 3, você pode usar \_ BX2 em qualquer registro de origem para qualquer \* instrução Tex, exceto: [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) ou [texbeml-PS](texbeml---ps.md).

## <a name="example"></a>Exemplo

Este exemplo amostra uma textura, converte dados no intervalo de-1 a + 1 e calcula um produto de ponto.


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




