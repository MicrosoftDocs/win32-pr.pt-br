---
title: Propriedade de volume IWMPSettings
description: A propriedade volume Obtém ou define o volume de reprodução atual.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Propriedade de volume Windows Media Player
- Propriedade de volume Windows Media Player, interface IWMPSettings
- Interface IWMPSettings do Windows Media Player, propriedade de volume
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
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782870"
---
# <a name="iwmpsettingsvolume-property"></a>Propriedade IWMPSettings:: volume

A propriedade **volume** Obtém ou define o volume de reprodução atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o nível de volume, variando de 0 a 100.

## <a name="remarks"></a>Comentários

Um valor de zero não especifica nenhum volume (mudo). Um valor de 100 especifica o volume completo. Se nenhum valor for especificado para essa propriedade, o padrão será a última configuração de volume estabelecida para o Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





