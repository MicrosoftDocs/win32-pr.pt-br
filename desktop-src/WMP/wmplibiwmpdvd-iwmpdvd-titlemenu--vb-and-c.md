---
title: Método IWMPDVD titleMenu
description: O método titleMenu para a reprodução e exibe o menu título.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- método titleMenu Windows Media Player
- método titleMenu Windows Media Player, interface IWMPDVD
- Interface IWMPDVD Windows Media Player, método titleMenu
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
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748307"
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

## <a name="return-value"></a>Retornar valor

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

 

 





