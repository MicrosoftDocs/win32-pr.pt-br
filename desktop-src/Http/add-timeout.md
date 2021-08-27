---
title: add timeout
description: Adiciona um tempo limite global ao serviço de HTTP.sys.
ms.assetid: c59a64e2-36aa-4428-b727-df21f5632d0d
keywords:
- Adicionar tempo limite HTTP
topic_type:
- apiref
api_name:
- add timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66a136acf65022ccc3ba8b05d070e4855a64f7abdf9b0519f7c1628d292aa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047596"
---
# <a name="add-timeout"></a>add timeout

Adiciona um tempo limite global ao serviço de HTTP.sys.

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleConnectionTimeout \| HeaderWaitTimeout}**
</dt> <dd>

Especifica o tipo de tempo limite para configuração.

</dd> <dt>

<span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>**\[ valor = \]**_u-curto_
</dt> <dd>

Especifica o valor do tempo limite (em segundos). Se value for hexadecimal, adicione o prefixo 0x.

</dd> </dl>

## <a name="examples"></a>Exemplos

**add timeout timeouttype=idleconnectiontimeout value=120**

**add timeout timeouttype=headerwaittimeout value=0x40**

 

 




