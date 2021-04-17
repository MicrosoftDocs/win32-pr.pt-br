---
title: Propriedade AxWindowsMediaPlayer. stretchToFit
description: A propriedade stretchToFit Obtém ou define um valor que indica se o vídeo exibido pelo controle do Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Propriedade stretchToFit Windows Media Player
- Propriedade stretchToFit Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade stretchToFit
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759740"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>Propriedade AxWindowsMediaPlayer. stretchToFit

A propriedade stretchToFit Obtém ou define um valor que indica se o vídeo exibido pelo controle do Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

O valor System. Boolean que indica se o vídeo será alongado para se ajustar à janela. O valor padrão é false.

## <a name="remarks"></a>Comentários

Quando **stretchToFit** é definido como true, o controle do Windows Media Player mantém a taxa de proporção original do vídeo. Se a taxa de proporção do vídeo não corresponder à taxa de proporção da janela de vídeo, as áreas de máscara preta poderão aparecer na parte superior e inferior, ou à esquerda e à direita da imagem de vídeo.

Essa propriedade se aplica ao controle do Windows Media Player somente quando ele é inserido em uma página da Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





