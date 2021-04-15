---
description: A classe CImageDisplay é uma classe auxiliar para renderizadores de vídeo GDI gerenciar o formato de exibição.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Classe CImageDisplay (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760769"
---
# <a name="cimagedisplay-class"></a>Classe CImageDisplay

![cimagedisplayclasshierarchy](images/wutil06.png)

A `CImageDisplay` classe é uma classe auxiliar para renderizadores de vídeo GDI gerenciar o formato de exibição. O objeto armazena uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que descreve o modo de exibição atual, que é inicializado no método de construtor do objeto. O método **CheckMediaType** do objeto verifica se um tipo de mídia proposto pode ser renderizado com eficiência usando GDI.



| Variáveis de membro protegido                                       | Descrição                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_exibição m**](cimagedisplay-m-display.md)                    | Estrutura **VIDEOINFO** que descreve o formato de exibição atual.                     |
| Métodos Protegidos                                                | Descrição                                                                            |
| [**CheckBitFields**](cimagedisplay-checkbitfields.md)           | Valida as máscaras de cores em uma estrutura **VIDEOINFO** .                                |
| [**CountPrefixBits**](cimagedisplay-countprefixbits.md)         | Calcula o número de zero bits no início de um campo de bits especificado.              |
| [**CountSetBits**](cimagedisplay-countsetbits.md)               | Retorna o número de bits definido como 1 em um campo de bit especificado.                          |
| Métodos públicos                                                   | Descrição                                                                            |
| [**CheckHeaderValidity**](cimagedisplay-checkheadervalidity.md) | Valida uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .                    |
| [**CheckMediaType**](cimagedisplay-checkmediatype.md)           | Determina se um tipo de mídia proposto é compatível com o formato de exibição.        |
| [**CheckPaletteHeader**](cimagedisplay-checkpaletteheader.md)   | Valida as entradas da paleta em uma estrutura **VIDEOINFO** .                            |
| [**CheckVideoType**](cimagedisplay-checkvideotype.md)           | Verifica se um formato **VIDEOINFO** especificado é compatível com o formato de exibição. |
| [**CImageDisplay**](cimagedisplay-cimagedisplay.md)             | Método de construtor.                                                                    |
| [**Getbitmasks**](cimagedisplay-getbitmasks.md)                 | Recupera as máscaras de cores para um formato **VIDEOINFO** especificado.                        |
| [**GetColourMask**](cimagedisplay-getcolourmask.md)             | Recupera as máscaras de cores para o formato de exibição atual.                              |
| [**GetDisplayDepth**](cimagedisplay-getdisplaydepth.md)         | Recupera a profundidade de bits do modo de exibição atual.                                   |
| [**GetDisplayFormat**](cimagedisplay-getdisplayformat.md)       | Recupera um formato de vídeo que descreve o modo de exibição atual.                      |
| [**IsPalettised**](cimagedisplay-ispalettised.md)               | Retermines se o formato de exibição atual é palettized.                           |
| [**RefreshDisplayType**](cimagedisplay-refreshdisplaytype.md)   | Atualiza o formato de vídeo do objeto para corresponder à exibição especificada                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




