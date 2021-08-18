---
title: texdp3tex-PS
description: Executa um produto de três componentes e usa o resultado para fazer uma pesquisa de textura 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91014b52b04417bbb23e76988beeb0bd4c473bd1e1d116433a8fd1dbf09a47ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788032"
---
# <a name="texdp3tex---ps"></a>texdp3tex-PS

Executa um produto de três componentes e usa o resultado para fazer uma pesquisa de textura 1D.

## <a name="syntax"></a>Syntax



| texdp3tex DST, src |
|--------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3tex             |      | x    | x    |      |      |      |       |      |       |



 

Os registros de textura devem usar a sequência a seguir.


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



Veja mais detalhes sobre como o produto e a pesquisa de textura do ponto são feitos.

A instrução texdp3tex executa um produto de três componentes, ponto.

u ' = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

O resultado é usado para exemplificar a textura no estágio de textura m executando uma pesquisa 1D.

t (m)<sub>RGBA</sub> = TextureSample (estágio m)<sub>RGBA</sub> usando (u ', 0, 0) como coordenadas

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




