---
title: Método AxWindowsMediaPlayer.openPlayer
description: O método openPlayer é aberto Windows Media Player usando a URL especificada. | Método AxWindowsMediaPlayer.openPlayer
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- Método openPlayer Windows Media Player
- Método openPlayer Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , método openPlayer
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a2ae5660969e78aeb165c5f9fd9420ea04c79a6aeec9a57c4627cd61d32ef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764706"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>Método AxWindowsMediaPlayer.openPlayer

O **método openPlayer** é aberto Windows Media Player usando a URL especificada.

## <a name="syntax"></a>Sintaxe


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Bstrurl* 
</dt> <dd>

O **System.String** que é a URL do item de mídia a ser reproduzir.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método inicia Windows Media Player com a URL especificada definida como o item de mídia atual. Se o Player tiver sido fechado anteriormente no modo de capa, ele será aberto usando a capa escolhida pela última vez pelo usuário. Caso contrário, o Player será aberto no modo completo.

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

 

 





