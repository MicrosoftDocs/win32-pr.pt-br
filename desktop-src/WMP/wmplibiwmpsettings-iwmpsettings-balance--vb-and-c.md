---
title: Propriedade de saldo de IWMPSettings
description: A propriedade Balance Obtém ou define o saldo do estéreo atual.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- Propriedade Balance Windows Media Player
- Propriedade Balance Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, Propriedade Balance
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
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765031"
---
# <a name="iwmpsettingsbalance-property"></a>Propriedade IWMPSettings:: Balance

A propriedade **Balance** Obtém ou define o saldo do estéreo atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o valor de saldo. Esse valor pode variar de 100 a 100. O valor padrão é zero.

## <a name="remarks"></a>Comentários

O valor zero indica que o áudio é reproduzido em um volume igual nos canais esquerdo e direito. Um valor de 100 indica que o áudio é reproduzido somente no canal à esquerda. Um valor de 100 indica que o áudio é reproduzido somente no canal correto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





