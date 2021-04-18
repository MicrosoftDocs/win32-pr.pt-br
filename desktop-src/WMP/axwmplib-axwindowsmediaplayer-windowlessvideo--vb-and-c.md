---
title: Propriedade AxWindowsMediaPlayer. windowlessVideo
description: A propriedade windowlessVideo Obtém ou define um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- Propriedade windowlessVideo Windows Media Player
- Propriedade windowlessVideo Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade windowlessVideo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759739"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>Propriedade AxWindowsMediaPlayer. windowlessVideo

A propriedade windowlessVideo Obtém ou define um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

Um valor System. booliano que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela. O valor padrão é false.

## <a name="remarks"></a>Comentários

Por padrão, um controle do Windows Media Player inserido renderiza o vídeo em sua própria janela dentro da área do cliente. Quando **windowlessVideo** é definido como true, o objeto do Windows Media Player renderiza o vídeo diretamente na área do cliente, para que você possa aplicar efeitos especiais ou colocar em camadas o vídeo com texto.

No Windows Vista, o vídeo de renderização no modo sem janela pode prejudicar o desempenho.

Não há suporte para a obtenção de um valor para essa propriedade no Netscape Navigator. Definir um valor para essa propriedade no Netscape Navigator pode gerar resultados inesperados.

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

 

 





