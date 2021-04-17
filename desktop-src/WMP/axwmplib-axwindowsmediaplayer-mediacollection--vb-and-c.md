---
title: Propriedade AxWindowsMediaPlayer. mediacollection
description: A propriedade mediacollection Obtém uma interface IWMPMediaCollection que fornece uma maneira de organizar uma grande coleção de itens de mídia.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- Propriedade mediacollection Windows Media Player
- Propriedade mediacollection Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade mediacollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762101"
---
# <a name="axwindowsmediaplayermediacollection-property"></a>Propriedade AxWindowsMediaPlayer. mediacollection

A propriedade mediacollection Obtém uma interface **IWMPMediaCollection** que fornece uma maneira de organizar uma grande coleção de itens de mídia.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a>Valor da propriedade

A interface WMPLib. IWMPMediaCollection para uma coleção de itens de mídia.

## <a name="remarks"></a>Comentários

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

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

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





