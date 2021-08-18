---
title: RPC_NS_HANDLE (Rpcnsi.h)
description: O tipo de dados RPC \_ NS \_ HANDLE define um identificador nome-serviço.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7612671b03f507bc2e722520fa775e0e999d0f1456ebfcefa971bba27b65dbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926280"
---
# <a name="rpc_ns_handle"></a>RPC \_ NS \_ HANDLE

O tipo de **dados RPC \_ NS \_ HANDLE** define um identificador nome-serviço.


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a>Comentários

Um nome-serviço handle é uma variável opaca que contém informações que a biblioteca de tempo de executar RPC usa para retornar os seguintes dados RPC do banco de dados name-service:

-   Alças de associação de servidor
-   UUIDs de recursos oferecidos por membros do perfil de servidor
-   Membros do grupo

O escopo de um nome-serviço é de uma rotina "Begin" até a rotina "Done" correspondente.

Os aplicativos são responsáveis pelo controle de concurreência de alças de nome-serviço entre threads.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcnsi.h (inclua Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcNsBindingLookupDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





