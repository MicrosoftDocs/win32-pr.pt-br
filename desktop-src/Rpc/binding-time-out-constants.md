---
title: Constantes de tempo-de-tempo de associação (Rpcdce.h)
description: A biblioteca RPC usa as constantes de tempo-limites de associação para especificar a quantidade relativa de tempo que deve ser gasto para estabelecer uma associação ao servidor antes de abrir mão.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125a38dd41445ba0661d13c61e7c79e689bc29abffa535791b233c40cfb704ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932357"
---
# <a name="binding-time-out-constants"></a>Constantes de tempo-de-tempo de associação

A biblioteca RPC usa as constantes de tempo-limites de associação para especificar a quantidade relativa de tempo que deve ser gasto para estabelecer uma associação ao servidor antes de abrir mão. O tempoout pode ser habilitado com uma chamada para a [**função RpcMgmtSetComTimeout.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) A lista a seguir contém os valores de tempo-out válidos.



| Constante/valor                                                                                                                                                                                                                                                                | Descrição                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ INFINITE \_ TIMEOUT**</dt> <dt> 10</dt> </dl> | Continua tentando estabelecer comunicações para sempre.<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ MIN \_ TIMEOUT**</dt> <dt>0</dt> </dl>                   | Tenta a quantidade mínima de tempo para o protocolo de rede que está sendo usado. Esse valor favorece o tempo de resposta sobre a correção ao determinar se o servidor está em execução.<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ DEFAULT \_ TIMEOUT**</dt> <dt>5</dt> </dl>       | Tenta uma quantidade média de tempo para o protocolo de rede que está sendo usado. Esse valor fornece corretamente ao determinar se um servidor está em execução e fornece o mesmo peso ao tempo de resposta. Esse é o valor padrão.<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ MAX \_ TIMEOUT**</dt> <dt>9</dt> </dl>                   | Tenta a maior quantidade de tempo para o protocolo de rede que está sendo usado. Esse valor favorece a correção ao determinar se um servidor está sendo executado durante o tempo de resposta.<br/>                                            |



## <a name="remarks"></a>Comentários

Os valores na tabela anterior não estão em segundos. Esses valores representam uma quantidade relativa de tempo em uma escala de zero a 10. Para obter mais informações sobre como evitar atrasos de comunicação, consulte Prevenindo travamentos do lado do cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



 

 





