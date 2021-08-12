---
title: Propriedade AxWindowsMediaPlayer.windowlessVideo
description: A propriedade windowlessVideo obtém ou define um valor que indica se o controle Windows Media Player renderiza o vídeo no modo sem janela.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- propriedade windowlessVideo Windows Media Player
- propriedade windowlessVideo Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , propriedade windowlessVideo
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
ms.openlocfilehash: 3a63a7246e730f73bd6d6f27111112a3db2029e3b53c80569e2e013771da6708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581516"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>Propriedade AxWindowsMediaPlayer.windowlessVideo

A propriedade windowlessVideo obtém ou define um valor que indica se o controle Windows Media Player renderiza o vídeo no modo sem janela.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

Um valor System.Boolean que indica se o controle Windows Media Player renderiza o vídeo no modo sem janela. O valor padrão é false.

## <a name="remarks"></a>Comentários

Por padrão, um controle Windows Media Player inserido renderiza o vídeo em sua própria janela na área do cliente. Quando **windowlessVideo** é definido como true, o objeto Windows Media Player renderiza o vídeo diretamente na área do cliente, para que você possa aplicar efeitos especiais ou colocar o vídeo em camadas com texto.

No Windows Vista, renderizar vídeo no modo sem janela pode prejudicar o desempenho.

Não há suporte para obter um valor para essa propriedade no Netscape Navigator. Definir um valor para essa propriedade no Netscape Navigator pode gerar resultados inesperados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





