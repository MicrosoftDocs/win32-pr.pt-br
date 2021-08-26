---
description: Os seguintes subtipos definem formatos RGB não compactados sem canal alfa.
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: Subtipos de vídeo RGB não compactados (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8fc35faaa5b6a58a597bf8d563ded4a920b0a112f61a4858f32c1b61fa29966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130976"
---
# <a name="uncompressed-rgb-video-subtypes"></a>Subtipos de vídeo RGB não compactados

Os seguintes subtipos definem formatos RGB não compactados sem canal alfa.



| Constante                                                                                                                                                                        | Descrição                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**MEDIASUBTYPE \_ RGB1**</dt> </dl>       | RGB, 1 bit por pixel (BPP), palettized<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**MEDIASUBTYPE \_ RGB4**</dt> </dl>       | RGB, 4 BPP, palettized<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**MEDIASUBTYPE \_ RGB8**</dt> </dl>       | RGB, 8 bpp, palettized<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**MEDIASUBTYPE \_ RGB555**</dt> </dl> | RGB 555, 16 BPP<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**MEDIASUBTYPE \_ RGB565**</dt> </dl> | RGB 565, 16 BPP<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**MEDIASUBTYPE \_ RGB24**</dt> </dl>    | RGB, 24 bpp<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**MEDIASUBTYPE \_ RGB32**</dt> </dl>    | RGB, 32 bpp<br/>                            |



Os seguintes subtipos definem formatos RGB não compactados com o canal alfa.



| Constante                                                                                                                                                                                       | Descrição                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB1555**</dt> </dl>          | RGB 555 com canal alfa<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB32**</dt> </dl>                | RGB 32 com canal alfa<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB4444**</dt> </dl>          | RGB de 16 bits com canal alfa; 4 bits por canal<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**MEDIASUBTYPE \_ A2R10G10B10**</dt> </dl> | RGB de 32 bits com canal alfa; 10 bits por canal RGB mais 2 bits para alfa.<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**MEDIASUBTYPE \_ A2B10G10R10**</dt> </dl> | BGR-bit de 32 bits com canal alfa; 10 bits por canal BGR mais 2 bits para alfa.<br/> |



## <a name="remarks"></a>Comentários

Para formatos palettized, a cor de cada pixel é especificada como um índice em uma paleta. A paleta deve ser incluída no bloco de formato, após a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Para formatos não palettized, a cor de cada pixel é especificada diretamente; o layout da memória depende da profundidade de bits:

-   O RGB 555 usa o seguinte layout de memória:
    ```C++
    High-order byte:    Low-order byte: 
    X R R R R R G G     G G G B B B B B 

    X = Don't care, R = Red, G = Green, B = Blue
    ```

    

-   O RGB 565 usa o seguinte layout de memória:
    ```C++
    High-order byte:    Low-order byte: 
    R R R R R G G G     G G G B B B B B 
    ```

    

-   Para o RGB 24, cada pixel é um [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple). Cada cor é de um byte, com um valor de 0 a 255, inclusive. O layout de memória é:

    |       | Layout     | Layout      | Layout     |
    |-------|------|-------|-----|
    | **Byte**  | 0    | 1     | 2   |
    | **Valor** | Azul | Verde | Vermelho |

    

     

-   Para o RGB 32, cada pixel é um **RGBQUAD**. Cada cor é de um byte, com um valor de 0 a 255, inclusive. O layout de memória é: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|------|-------|-----|---------------------|
    | **Byte**  | 0    | 1     | 2   | 3                   |
    | **Valor** | Azul | Verde | Vermelho | Alfa ou não se preocupe |

    

     

    Se o subtipo for MEDIASUBTYPE \_ ARGB32, byte 3 conterá um valor para o canal alfa. Se o subtipo for MEDIASUBTYPE \_ RGB32, byte 3 deverá ser ignorado.

-   A2R10G10B10 usa o seguinte layout: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|-------|---------|---------|---------|
    | **Parte**   | 0 – 9 | 10 – 19 | 20 - 29 | 30 - 31 |
    | **Valor** | Azul  | Verde   | Vermelho     | Alpha   |

    

     

-   A2B10G10R10 usa o seguinte layout: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|-------|---------|---------|---------|
    | **Parte**   | 0 – 9 | 10 – 19 | 20 - 29 | 30 - 31 |
    | **Valor** | Vermelho   | Verde   | Azul    | Alpha   |

    

     

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> <dt>

[Trabalhando com quadros de vídeo](working-with-video-frames.md)
</dt> </dl>

 

 
