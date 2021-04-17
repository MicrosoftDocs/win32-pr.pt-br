---
title: Método de back IWMPDVD
description: O método back altera a exibição de um submenu para seu menu pai.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- método de back Windows Media Player
- método de back Windows Media Player, interface IWMPDVD
- Interface IWMPDVD Windows Media Player, método back
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755459"
---
# <a name="iwmpdvdback-method"></a>Método IWMPDVD:: back

O método **back** altera a exibição de um submenu para seu menu pai.

## <a name="syntax"></a>Sintaxe


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada DVD é criado de maneira diferente. Alguns DVDs são criados para que o `back` método esteja disponível no menu raiz, mas quando invocado, ele não fará nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





