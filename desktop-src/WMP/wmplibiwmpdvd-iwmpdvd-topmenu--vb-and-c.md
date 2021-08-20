---
title: Método IWMPDVD topMenu
description: O método topMenu para a reprodução e exibe o menu superior (ou raiz) do título atual.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- Windows Media Player do método topMenu
- método topMenu Windows Media Player, interface IWMPDVD
- Windows Media Player de interface IWMPDVD, método topMenu
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f9cc1dcd528b93e9959f63a387747e510f7dd57b403ad70e41768d77006337
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930208"
---
# <a name="iwmpdvdtopmenu-method"></a>Método IWMPDVD:: topMenu

O método **topMenu** para a reprodução e exibe o menu superior (ou raiz) do título atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada DVD é criado de maneira diferente. O DVD deve conter um menu para que esse método funcione. Alguns DVDs são criados para que os métodos **topMenu** e **IWMPDVD. titleMenu** Abram o mesmo menu. O método **topMenu** geralmente invoca o menu superior (ou raiz), mas ele pode invocar o menu de título se não houver nenhum menu raiz disponível.

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

[**IWMPDVD. titleMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





