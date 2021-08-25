---
description: O método UOPValid recupera um valor que indica se a UOP (operação de usuário) especificada é válida no momento.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Método UOPValid (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eee8f11fbcc51c982b2a619f35fdd56b0f0eebe86945e84f18d6ce62afa783b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078666"
---
# <a name="uopvalid-method"></a>Método UOPValid

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O método recupera um valor que indica se a `UOPValid` UOP (operação de usuário) especificada é válida no momento.

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*
</dt> <dd>

Especifica a UOP (operação do usuário) como um Inteiro.



| Valor | Descrição                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**PlayTitle,**](playtitle-method.md) [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)                                                                                      |
| 1     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**PlayTitle**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**Stop**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**ReturnFromSubmenu**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**PlayPrevChapter,**](playprevchapter-method.md) [ **ReplayChapter**](replaychapter-method.md)                                                                                                                         |
| 7     | [**PlayNextChapter**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**PlayForwards**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**PlayBackwards**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [**ShowMenu com**](showmenu-method.md) um valor de parâmetro 2 (título \_ do MENU DE \_ DVD)                                                                                                                                       |
| 11    | [**ShowMenu com**](showmenu-method.md) um valor de parâmetro de 3 (RAIZ \_ DO MENU DE \_ DVD)                                                                                                                                        |
| 12    | [**ShowMenu com**](showmenu-method.md) um valor de parâmetro de 4 \_ (subtípico menu \_ de DVD)                                                                                                                                  |
| 13    | [**ShowMenu com**](showmenu-method.md) um valor de parâmetro 5 (ÁUDIO \_ DO MENU DE \_ DVD)                                                                                                                                       |
| 14    | [**ShowMenu com**](showmenu-method.md) um valor de parâmetro de 6 (ângulo \_ do MENU DE \_ DVD)                                                                                                                                       |
| 15    | [**ShowMenu com**](showmenu-method.md) um valor de parâmetro de 7 (capítulo \_ menu de \_ DVD)                                                                                                                                     |
| 16    | [**Retomar**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**SelectLeftButton,**](selectleftbutton-method.md) [**SelectRightButton,**](selectrightbutton-method.md) [**SelectUpperButton,**](selectupperbutton-method.md) [**SelectLowerButton**](selectlowerbutton-method.md) |
| 18    | [**StillOff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Pausar**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**CurrentAudioStream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**CurrentSubpictureStream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**CurrentAngle,**](currentangle-property.md) [ **SelectParentalLevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**LtdeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Selecione preferência de modo de vídeo.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliana que indica se a operação especificada é permitida pelo controle UOP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment.h</dt> </dl> |



 

 




