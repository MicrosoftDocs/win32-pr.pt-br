---
title: Bem-PS
description: Aplicar um ambiente de relevo falso – transformação de mapa.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fdc28e6eaf71156504306b247a1a2a3797423f9a7e3bde6d4040ecb1297e09da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794817"
---
# <a name="bem---ps"></a>Bem-PS

Aplicar um ambiente de relevo falso – transformação de mapa.

## <a name="syntax"></a>Syntax



| Bem DST. RG, src0, src1 |
|------------------------|



 

onde

-   DST. RG DST é o registro de destino. A máscara de gravação do componente vermelho e verde deve ser usada.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bem                   |      |      |      | x    |      |      |       |      |       |



 

Essa instrução executa o cálculo a seguir.


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



Regras para usar bem:

1.  Bem deve aparecer na primeira fase de um sombreador (ou seja, antes de um marcador de fase).
2.  Bem consome dois slots de instrução aritméticos.
3.  Somente um uso desta instrução é permitido por sombreador.
4.  Writemask de destino deve ser. RG/.XY.
5.  Esta instrução não pode ser emitida em conjunto.
6.  Além da restrição que a máscara de gravação de destino é. RG, os modificadores nos modificadores de origem src0, src1 e instrução são irrestrito.

## <a name="instruction-information"></a>Informações de instrução



| Requisito                         | Valor           |
|--------------------------|------------|
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




