---
title: delete timeout
description: Exclui um tempo limite global e faz com que o serviço de HTTP.sys reverta para os valores padrão.
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- excluir tempo limite HTTP
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6ee436e1eb7f545a74aa56f6c146afbd1c57066
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "105766910"
---
# <a name="delete-timeout"></a>delete timeout

Exclui um tempo limite global e faz com que o serviço de HTTP.sys reverta para os valores padrão.

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleConnectionTimeout \| HeaderWaitTimeout}**
</dt> <dd>

Especifica o tipo de configuração de tempo limite.

</dd> </dl>

## <a name="examples"></a>Exemplos

**delete timeout timeouttype=idleconnectiontimeout**

**delete timeout timeouttype=headerwaittimeout**

 

 




