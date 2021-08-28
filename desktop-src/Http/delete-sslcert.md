---
title: delete sslcert
description: Exclui as vinculações de certificado do servidor SSL e as políticas de certificado do cliente correspondentes para um endereço IP e uma porta.
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- delete sslcert HTTP
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45d811bedfa1d2a228cd29decf2272d85b8ca6de5c1d27656b3e37b8d6b4d4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870536"
---
# <a name="delete-sslcert"></a>delete sslcert

Exclui as vinculações de certificado do servidor SSL e as políticas de certificado do cliente correspondentes para um endereço IP e uma porta.

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ ipport= \]**_Endereço IP:porta_
</dt> <dd>

Especifica o endereço IPv4 ou IPv6 e a porta para a qual as vinculações de certificado SSL serão excluídas.

</dd> </dl>

## <a name="examples"></a>Exemplos

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**delete sslcert ipport= \[ :: \] :443**

 

 




