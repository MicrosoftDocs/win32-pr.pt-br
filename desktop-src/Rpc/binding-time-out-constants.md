---
title: Constantes de tempo limite de associação (rpcdce. h)
description: A Biblioteca RPC usa as constantes de tempo limite de associação para especificar a quantidade de tempo relativa que deve ser gasta para estabelecer uma associação ao servidor antes de desistir.
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
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105785392"
---
# <a name="binding-time-out-constants"></a>Constantes de tempo limite de associação

A Biblioteca RPC usa as constantes de tempo limite de associação para especificar a quantidade de tempo relativa que deve ser gasta para estabelecer uma associação ao servidor antes de desistir. O tempo limite pode ser habilitado com uma chamada para a função [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) . A lista a seguir contém os valores de tempo limite válidos.



| Constante/valor                                                                                                                                                                                                                                                                | Descrição                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Tempo limite infinito de associação C**</dt> <dt> 10</dt> </dl> | Continua tentando estabelecer comunicações para sempre.<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Tempo limite mínimo de associação de C**</dt> <dt>0</dt> </dl>                   | Tenta a quantidade mínima de tempo para o protocolo de rede que está sendo usado. Esse valor favorece o tempo de resposta em relação à exatidão para determinar se o servidor está em execução.<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Tempo limite padrão de associação C**</dt> <dt>5</dt> </dl>       | Tenta uma quantidade média de tempo para o protocolo de rede ser usado. Esse valor fornece a exatidão para determinar se um servidor está em execução e dá um tempo de resposta igual a peso. Esse é o valor padrão.<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Tempo limite máximo de associação de C**</dt> <dt>9</dt> </dl>                   | Tenta a quantidade mais longa de tempo para o protocolo de rede que está sendo usado. Esse valor favorece a exatidão para determinar se um servidor está sendo executado no tempo de resposta.<br/>                                            |



## <a name="remarks"></a>Comentários

Os valores na tabela anterior não estão em segundos. Esses valores representam uma quantidade relativa de tempo em uma escala de zero a 10. Para obter mais informações sobre como evitar atrasos de comunicação, consulte impedindo os bloqueios do lado do cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





