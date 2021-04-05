---
title: RpcTryExcept (RPC. h)
description: A instrução RpcTryExcept fornece manipulação de exceção estruturada para aplicativos RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RPC RpcTryExcept
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085788"
---
# <a name="rpctryexcept"></a>RpcTryExcept

A instrução **RpcTryExcept** fornece manipulação de exceção estruturada para aplicativos RPC. Se qualquer uma das instruções do programa no **RpcTryExcept** causar uma exceção, as instruções no bloco de código [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) serão executadas. Todas as instruções **RpcTryExcept** devem ser terminadas pela instrução [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) .

Para obter mais informações, consulte [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

**Windows Vista e versões posteriores do Windows:** o [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) é recomendado para manipulação de exceção estruturada para as exceções mais comuns como uma alternativa para filtros personalizados com [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).  

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**RpcTryFinally**](rpctryfinally.md)
</dt> </dl>

 

