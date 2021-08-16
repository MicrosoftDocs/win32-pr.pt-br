---
title: Propriedade de volume IWMPSettings
description: A propriedade volume obtém ou define o volume de reprodução atual.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- propriedade volume Windows Media Player
- propriedade de volume Windows Media Player , interface IWMPSettings
- Interface IWMPSettings Windows Media Player , propriedade de volume
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2077547dd00b5c75b6ca77a966190db2bb3bb1bcde61d1f5c5b84c794af84e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568393"
---
# <a name="iwmpsettingsvolume-property"></a>Propriedade IWMPSettings::volume

A **propriedade volume** obtém ou define o volume de reprodução atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32 que** é o nível de volume, variando de 0 a 100.

## <a name="remarks"></a>Comentários

Um valor de zero não especifica nenhum volume (muted). Um valor de 100 especifica o volume completo. Se nenhum valor for especificado para essa propriedade, o padrão será a última configuração de volume estabelecida para Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





