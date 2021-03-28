---
title: texldd-PS
description: Amostra uma textura com entradas de gradiente adicionais.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366040"
---
# <a name="texldd---ps"></a>texldd-PS

Amostra uma textura com entradas de gradiente adicionais.

## <a name="syntax"></a>Syntax



| texldd, DST, src0, src1, src2, src3 |
|-------------------------------------|



 

Em que:

-   o DST é um registro de destino.
-   src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura. Consulte [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifica os registros de amostra de origem \# , em que \# especifica qual número de amostra de textura deve ser amostrado. O classificador foi associado a ele uma textura e um estado de controle definido pela enumeração [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por exemplo, D3DSAMP \_ MINFILTER).
-   src2 é um registro de fonte de entrada que especifica o gradiente x.
-   src3 é um registro de fonte de entrada que especifica o gradiente y.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldd                |      |      |      |      |      | w.x.y. \* | x     | x    | x     |



 

\* Essa instrução só tem suporte no PS \_ 2 \_ a. Não há suporte para ele no PS \_ 2 \_ b. Para obter mais informações sobre perfis, consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).

Esta instrução amostra uma textura usando as coordenadas de textura em src0, a amostra especificada por src1 e os gradientes DSX e DSY provenientes de src2 e src3. Os valores de gradiente x e y são usados para selecionar o nível de mipmap apropriado da textura para amostragem.

Todas as fontes dão suporte a swizzles arbitrários.

Todas as máscaras de gravação são válidas no destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 