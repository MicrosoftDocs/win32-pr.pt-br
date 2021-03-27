---
title: texdp3-PS
description: Executa um produto de três componentes de ponto entre os dados no número de registro de textura e o conjunto de coordenadas de textura correspondente ao número de registro de destino.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293552"
---
# <a name="texdp3---ps"></a>texdp3-PS

Executa um produto de três componentes de ponto entre os dados no número de registro de textura e o conjunto de coordenadas de textura correspondente ao número de registro de destino.

## <a name="syntax"></a>Syntax



| texdp3 DST, src |
|-----------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3                |      | x    | x    |      |      |      |       |      |       |



 

Os registros de textura devem usar a sequência a seguir.


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



Veja mais detalhes sobre como o produto dot é realizado.

A instrução texdp3 executa um produto de três componentes e o Replica para todos os quatro canais de cores.

t (m)<sub>RGBA</sub> = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




