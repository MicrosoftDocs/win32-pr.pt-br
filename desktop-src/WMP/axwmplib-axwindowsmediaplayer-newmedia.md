---
title: Método AxWindowsMediaPlayer.newMedia
description: O método newMedia retorna uma interface IWMPMedia para um novo item de mídia.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- Método newMedia Windows Media Player
- newMedia method Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , método newMedia
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
ms.openlocfilehash: cdde19a6cb5da5113cb580c1916052c7ae0d38756bbc120368ffdfd464105591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618736"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>Método AxWindowsMediaPlayer.newMedia

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

*Bstrurl* 
</dt> <dd>

Um **System.String que** é a URL do arquivo de mídia digital usado para inicializar o novo item de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma interface WMPLib.IWMPMedia que representa o item de mídia recém-criado.

## <a name="remarks"></a>Comentários

O *parâmetro bstrURL* não deve ser uma cadeia de caracteres de comprimento zero ("") ou nula.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





