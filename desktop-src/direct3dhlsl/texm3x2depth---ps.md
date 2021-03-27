---
title: texm3x2depth-PS
description: Calcule o valor de profundidade a ser usado em testes de profundidade para este pixel.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967109"
---
# <a name="texm3x2depth---ps"></a>texm3x2depth-PS

Calcule o valor de profundidade a ser usado em testes de profundidade para este pixel.

## <a name="syntax"></a>Syntax



| texm3x2depth DST, src |
|-----------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2depth          |      |      | x    |      |      |      |       |      |       |



 

Essa instrução deve ser usada com a instrução [texm3x2pad-PS](texm3x2pad---ps.md) .

Ao usar essas duas instruções, os registros de textura devem usar a sequência a seguir.


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



O cálculo de profundidade é feito após o uso de uma operação de produto de ponto para localizar z e w. Veja mais detalhes sobre como o cálculo de profundidade é realizado.

A instrução texm3x2pad calcula z.

z = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

A instrução texm3x2depth calcula w.

w = TextureCoordinates (estágio m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Calcule a profundidade e armazene o resultado em t (m + 1).


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



A profundidade calculada é marcada para ser usada no teste de profundidade do pixel, substituindo o valor de teste de profundidade existente para o pixel.

Certifique-se de que fixe z/w esteja no intervalo de (0-1). Se z/w estiver fora desse intervalo, o resultado armazenado no buffer de profundidade será indefinido.

Depois de executar o texm3x2depth, o registro t (m + 1) não estará mais disponível para uso no sombreador.

Quando a multiamostragem, o uso dessa instrução elimina a maior parte do benefício do buffer de profundidade de resolução mais alto. Como o sombreador de pixel é executado uma vez por pixel, a saída de valor de profundidade única por texm3x2depth ou [texdepth-PS](texdepth---ps.md) será usada para cada um dos testes de comparação de profundidade de subpixel.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




