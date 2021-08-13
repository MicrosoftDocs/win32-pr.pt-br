---
description: Representa o método que é chamado quando uma ação assíncrona é concluída.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Interface AsyncActionCompletedHandler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 5d7e091ab250dc8b7475dbf17a1d1502cd1c4aa110106584c8c8b190c927f4aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561171"
---
# <a name="asyncactioncompletedhandler-interface"></a>Interface AsyncActionCompletedHandler

Representa o método que é chamado quando uma ação assíncrona é concluída.

## <a name="members"></a>Membros

A interface **AsyncActionCompletedHandler** herda de [**IAsyncInfo.**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo) **AsyncActionCompletedHandler** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **AsyncActionCompletedHandler** tem esses métodos.



| Método                                               | Descrição                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Invoke**](asyncactioncompletedhandler-invoke.md) | Invoca o método que é chamado quando a ação assíncrona especificada é concluída.<br/> |



 

## <a name="remarks"></a>Comentários

Atribua **um AsyncActionCompletedHandler** a [**um IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) para receber uma notificação quando a ação assíncrona for concluída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                    |
| parâmetro<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

