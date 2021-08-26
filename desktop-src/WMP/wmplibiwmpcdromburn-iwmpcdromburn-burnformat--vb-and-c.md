---
title: Propriedade burnFormat IWMPCdromForm
description: A propriedade burnFormat obtém um valor que indica o tipo de CD a ser gravar.
ms.assetid: f60fcbd2-5d34-46f3-a2e2-29dac2ecf689
keywords:
- Propriedade burnFormat Windows Media Player
- propriedade burnFormat Windows Media Player , interface IWMPCdromForm
- Interface IWMPCdrom Ltda Windows Media Player , propriedade burnFormat
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnFormat
- IWMPCdromBurn.get_burnFormat
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d5dc4ff27b3650ee37f16a7e90eb535ebe373401363f8c93bd16d09061b7a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000536"
---
# <a name="iwmpcdromburnburnformat-property"></a>Propriedade IWMPCdrom Ltd::burnFormat

A **propriedade burnFormat** obtém um valor que indica o tipo de CD a ser gravar.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public WMPBurnFormat burnFormat {get;}
```


```VB

Public ReadOnly Property burnFormat As WMPBurnFormat
```





## <a name="property-value"></a>Valor da propriedade

Um **WMPLib.WMP Ltdaformat** que é um valor da enumeração **WMPIiFormat** que indica o tipo de CD a ser gravar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11<br/>                                                                             |
| Namespace<br/> | **WMPLib**<br/>                                                                                          |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib (Interop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdrom Ltda (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMP Ltdaformat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
</dt> </dl>

 

 





