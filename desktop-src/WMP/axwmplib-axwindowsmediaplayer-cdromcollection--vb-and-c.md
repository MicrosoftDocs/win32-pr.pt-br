---
title: Propriedade AxWindowsMediaPlayer.cdromCollection
description: A propriedade cdromCollection obtém uma interface IWMPCdromCollection que fornece acesso a uma coleção de unidades de CD ou DVD.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- Propriedade cdromCollection Windows Media Player
- Propriedade cdromCollection Windows Media Player classe , AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , propriedade cdromCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec885de319153383b82359e35208d19031fa7378749b39033402aba11f8dbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054996"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a>Propriedade AxWindowsMediaPlayer.cdromCollection

A propriedade cdromCollection obtém uma interface **IWMPCdromCollection** que fornece acesso a uma coleção de unidades de CD ou DVD.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a>Valor da propriedade

Uma interface WMPLib.IWMPCdromCollection.

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

[**Interface IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





