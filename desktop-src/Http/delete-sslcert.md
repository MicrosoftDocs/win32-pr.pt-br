---
title: delete sslcert
description: Exclui associações de certificado de servidor SSL e as políticas de certificado de cliente correspondentes para um endereço IP e porta.
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- excluir HTTP sslcert
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7672df5eee1634c41ff153435edcbecc58c2595
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103638736"
---
# <a name="delete-sslcert"></a>delete sslcert

Exclui associações de certificado de servidor SSL e as políticas de certificado de cliente correspondentes para um endereço IP e porta.

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * endereço IP: porta*
</dt> <dd>

Especifica o endereço IPv4 ou IPv6 e a porta para a qual as associações de certificado SSL serão excluídas.

</dd> </dl>

## <a name="examples"></a>Exemplos

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**excluir SSLCERT IPPORT = \[ ::: \] 443**

 

 




