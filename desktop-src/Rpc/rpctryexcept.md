---
title: RpcTryExcept (Rpc.h)
description: A instrução RpcTryExcept fornece tratamento de exceção estruturado para aplicativos RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RpcTryExcept RPC
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
ms.openlocfilehash: 0c7a73ca80eb342b9a23fcaa4b922afe8d19f00e1f22ab82f8c6027ecc43d76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925963"
---
# <a name="rpctryexcept"></a>RpcTryExcept

A **instrução RpcTryExcept** fornece tratamento de exceção estruturado para aplicativos RPC. Se qualquer uma das instruções de programa **no RpcTryExcept** causar uma exceção, as instruções no bloco de código [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) serão executadas. Todas **as instruções RpcTryExcept** devem ser encerradas pela [**instrução RpcEndExcept.**](/previous-versions/aa375629(v=vs.80))

Para obter mais informações, [**consulte RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

Windows Vista e versões posteriores do **Windows:**[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) é recomendado para tratamento de exceções estruturadas para as exceções mais comuns como uma alternativa a filtros personalizados com [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).  

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Rpc.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**RpcTryFinally**](rpctryfinally.md)
</dt> </dl>

 

