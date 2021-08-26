---
title: Propriedade AxWindowsMediaPlayer.mediaCollection
description: A propriedade mediaCollection obtém uma interface IWMPMediaCollection que fornece uma maneira de organizar uma grande coleção de itens de mídia.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- propriedade mediaCollection Windows Media Player
- propriedade mediaCollection Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player propriedade , mediaCollection
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
ms.openlocfilehash: 86ad0cc720c49926ddbd75fe71d47738a9e8af43fa97670a0b9915a50716ed0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902626"
---
# <a name="axwindowsmediaplayermediacollection-property"></a>Propriedade AxWindowsMediaPlayer.mediaCollection

A propriedade mediaCollection obtém uma interface **IWMPMediaCollection** que fornece uma maneira de organizar uma grande coleção de itens de mídia.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a>Valor da propriedade

A interface WMPLib.IWMPMediaCollection para uma coleção de itens de mídia.

## <a name="remarks"></a>Comentários

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

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

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





