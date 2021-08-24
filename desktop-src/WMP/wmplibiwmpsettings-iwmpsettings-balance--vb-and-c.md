---
title: Propriedade de saldo IWMPSettings
description: A propriedade balancear obtém ou define o saldo estéreo atual.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- balance property Windows Media Player
- balance property Windows Media Player , interface IWMPSettings
- Interface IWMPSettings Windows Media Player propriedade , balance
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d519d656be6b4974e2b4dd2707aafb2bb153f6b26bafe75de948d5e50c67b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861076"
---
# <a name="iwmpsettingsbalance-property"></a>Propriedade IWMPSettings::balance

A **propriedade balancear** obtém ou define o saldo estéreo atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32 que** é o valor de saldo. Esse valor pode variar de 100 a 100. O valor padrão é zero.

## <a name="remarks"></a>Comentários

O valor zero indica que o áudio é reproduzindo em volume igual nos canais esquerdo e direito. Um valor de 100 indica que o áudio é reproduzindo somente no canal esquerdo. Um valor de 100 indica que o áudio é reproduzindo somente no canal direito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player Série 9 ou posterior.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





