---
title: RPC_STATUS (Rpcdce.h)
description: O tipo de dados RPC \_ STATUS representa um tipo de código de status específico da plataforma.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93cc6f682dbb46b65fc261b738b94e8000f3a77d96c4bd65d1fead4bf8c0e17a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925983"
---
# <a name="rpc_status"></a>STATUS DE RPC \_

O tipo de dados **RPC \_ STATUS representa** um tipo de código de status específico da plataforma.


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a>Comentários

O **tipo \_ STATUS RPC** é retornado pela maioria das funções RPC e faz parte da definição de tipo de função [**\_ RPC OBJECT \_ INQ \_ FN.**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce.h (incluir Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FN \_ \_ do INQ DO OBJETO \_ RPC**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





