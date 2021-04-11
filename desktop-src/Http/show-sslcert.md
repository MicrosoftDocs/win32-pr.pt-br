---
title: show sslcert
description: Lista associações de certificado de servidor SSL e as políticas de certificado de cliente correspondentes para um endereço IP e porta.
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- Mostrar HTTP sslcert
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71c2faf370066f5ce8d5ce6a20b173a74d0f645
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104293454"
---
# <a name="show-sslcert"></a>show sslcert

Lista associações de certificado de servidor SSL e as políticas de certificado de cliente correspondentes para um endereço IP e porta.

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * endereço IP: porta*
</dt> <dd>

Especifica o endereço IPv4 ou IPv6 e a porta para a qual as associações de certificado SSL serão exibidas. Não especificar um ipport lista todas as associações.

</dd> </dl>

## <a name="examples"></a>Exemplos

**Mostrar SSLCERT IPPORT = \[ FE80:: 1 \] : 443**

**show sslcert ipport=1.1.1.1:443**

**show sslcert ipport=0.0.0.0:443**

**Mostrar SSLCERT IPPORT = \[ ::: \] 443**

 

 




