---
description: O método UOPValid recupera um valor que indica se a operação de usuário especificada (UOP) é válida no momento.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Método UOPValid (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810929"
---
# <a name="uopvalid-method"></a>Método UOPValid

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `UOPValid` método recupera um valor que indica se a operação de usuário especificada (UOP) é válida no momento.

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*
</dt> <dd>

Especifica a operação do usuário (UOP) como um inteiro.



| Valor | Descrição                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)                                                                                      |
| 1     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**PlayTitle**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**Stop**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**ReturnFromSubmenu**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)                                                                                                                         |
| 7     | [**PlayNextChapter**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**PlayForwards**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**PlayBackwards**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [**Menu**](showmenu-method.md) de propriedade com um valor de parâmetro 2 ( \_ título de menu de DVD \_ )                                                                                                                                       |
| 11    | [**Menu de atalho**](showmenu-method.md) com um valor de parâmetro de 3 (raiz do menu do DVD \_ \_ )                                                                                                                                        |
| 12    | [**Menu de menus**](showmenu-method.md) com um valor de parâmetro 4 ( \_ subimagem do menu DVD \_ )                                                                                                                                  |
| 13    | [**Menu de atalho**](showmenu-method.md) com um valor de parâmetro de 5 (áudio de menu de DVD \_ \_ )                                                                                                                                       |
| 14    | [**Menu de atalho**](showmenu-method.md) com um valor de parâmetro 6 ( \_ ângulo de menu de DVD \_ )                                                                                                                                       |
| 15    | [**Menu de atalho**](showmenu-method.md) com um valor de parâmetro de 7 (capítulo de menu do DVD \_ \_ )                                                                                                                                     |
| 16    | [**Retomar**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md) |
| 18    | [**StillOff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Pausar**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**CurrentAudioStream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**CurrentSubpictureStream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Selecione preferência de modo de vídeo.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano que indica se a operação especificada é permitida pelo controle UOP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment. h</dt> </dl> |



 

 




