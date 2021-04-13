---
title: RpcTryFinally (RPC. h)
description: A instrução RpcTryFinally fornece manipulação de terminação estruturada.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RPC RpcTryFinally
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455409"
---
# <a name="rpctryfinally"></a>RpcTryFinally

A instrução **RpcTryFinally** fornece manipulação de terminação estruturada. Ocorre uma exceção durante as instruções de execução do bloco de código associado à instrução **RpcTryFinally** , as instruções no bloco de código associado à instrução [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) são executadas. Todas as instruções **RpcTryFinally** devem ser terminadas por uma instrução [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) .

Para obter mais informações, consulte [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RpcFinally**](/previous-versions/aa375699(v=vs.80))
</dt> <dt>

[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))
</dt> </dl>

 

