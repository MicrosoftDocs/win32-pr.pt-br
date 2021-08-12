---
title: Propriedade AxWindowsMediaPlayer. stretchToFit
description: a propriedade stretchToFit obtém ou define um valor que indica se o vídeo exibido pelo controle de Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Windows Media Player da propriedade stretchToFit
- propriedade stretchToFit Windows Media Player, classe AxWindowsMediaPlayer
- classe AxWindowsMediaPlayer Windows Media Player, propriedade stretchToFit
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
ms.openlocfilehash: a3090889207e0631fbc2f35613398b4c979f4c907cfe240e9f0a7374c74b00b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581506"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>Propriedade AxWindowsMediaPlayer. stretchToFit

a propriedade stretchToFit obtém ou define um valor que indica se o vídeo exibido pelo controle de Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

O valor System. Boolean que indica se o vídeo será alongado para se ajustar à janela. O valor padrão é false.

## <a name="remarks"></a>Comentários

quando **stretchToFit** é definido como true, o controle de Windows Media Player mantém a taxa de proporção original do vídeo. Se a taxa de proporção do vídeo não corresponder à taxa de proporção da janela de vídeo, as áreas de máscara preta poderão aparecer na parte superior e inferior, ou à esquerda e à direita da imagem de vídeo.

essa propriedade se aplica ao controle de Windows Media Player somente quando ele é inserido em uma página da web.

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

 

 





