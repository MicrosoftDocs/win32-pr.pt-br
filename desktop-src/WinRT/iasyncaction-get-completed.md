---
description: Obtém o método que é chamado quando a ação assíncrona é concluída.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'Método IAsyncAction:: get_Completed'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090416"
---
# <a name="iasyncactionget_completed-method"></a>Método IAsyncAction:: get \_ Completed

Obtém o método que é chamado quando a ação assíncrona é concluída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*manipulador* \[ fora\]
</dt> <dd>

Tipo: **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***

O método que manipula a notificação de conclusão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                    |
| parâmetro<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
