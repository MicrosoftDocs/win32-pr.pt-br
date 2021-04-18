---
title: Método IWMPDVD topMenu
description: O método topMenu para a reprodução e exibe o menu superior (ou raiz) do título atual.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- método topMenu Windows Media Player
- método topMenu Windows Media Player, interface IWMPDVD
- Interface IWMPDVD Windows Media Player, método topMenu
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
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762470"
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

## <a name="return-value"></a>Retornar valor

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

 

 





