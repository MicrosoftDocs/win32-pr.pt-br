---
title: Método IWMPDVD titleMenu
description: O método titleMenu para a reprodução e exibe o menu título.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- Windows Media Player do método titleMenu
- método titleMenu Windows Media Player, interface IWMPDVD
- Windows Media Player de interface IWMPDVD, método titleMenu
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff485cd09915ec9acb076d2c06a8aa28c3549bf6527495e5e32d4a01d483285a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000456"
---
# <a name="iwmpdvdtitlemenu-method"></a>Método IWMPDVD:: titleMenu

O método **titleMenu** para a reprodução e exibe o menu título.

## <a name="syntax"></a>Sintaxe


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada DVD é criado de maneira diferente. O DVD deve conter um menu para que esse método funcione. Alguns DVDs são criados para que os métodos **IWMPDVD. topMenu** e **titleMenu** Abram o mesmo menu. O método **titleMenu** geralmente invoca o menu title, mas ele pode invocar o menu superior se não houver nenhum menu de título disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. topMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





