---
title: Método AxWindowsMediaPlayer. openPlayer
description: O método openPlayer abre o Windows Media Player usando a URL especificada. | Método AxWindowsMediaPlayer. openPlayer
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- método openPlayer Windows Media Player
- método openPlayer Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, método openPlayer
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
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813190"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>Método AxWindowsMediaPlayer. openPlayer

O método **openPlayer** abre o Windows Media Player usando a URL especificada.

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

*bstrURL* 
</dt> <dd>

O **System. String** que é a URL do item de mídia a ser reproduzido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método inicia o Windows Media Player com a URL especificada definida como o item de mídia atual. Se o Player foi fechado anteriormente no modo de capa, ele será aberto usando a capa escolhida pela última vez pelo usuário. Caso contrário, o Player será aberto no modo completo.

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

 

 





