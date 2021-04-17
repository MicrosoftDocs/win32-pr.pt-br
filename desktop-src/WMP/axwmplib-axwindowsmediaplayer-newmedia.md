---
title: Método AxWindowsMediaPlayer. newMedia
description: O método newMedia retorna uma interface IWMPMedia para um novo item de mídia.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- método newMedia Windows Media Player
- método newMedia Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, método newMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784915"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>Método AxWindowsMediaPlayer. newMedia

O método newMedia retorna uma interface IWMPMedia para um novo item de mídia.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrURL* 
</dt> <dd>

Um **System. String** que é a URL do arquivo de mídia digital usado para inicializar o novo item de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface WMPLib. IWMPMedia que representa o item de mídia recém-criado.

## <a name="remarks"></a>Comentários

O parâmetro *bstrURL* não deve ser uma cadeia de caracteres de comprimento zero ("") ou NULL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





