---
title: delete iplisten
description: Especifica um endereço IPv4 ou IPv6 a ser excluído da lista de escutas de IP.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- excluir iplisten HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42dbe9716ae19fdbbfb8f147b0f5f7f5a592adbf7b241c2f4e4548e0ee7e6e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014864"
---
# <a name="delete-iplisten"></a>delete iplisten

Especifica um endereço IPv4 ou IPv6 a ser excluído da lista de escutas de IP.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ address= \]** *IPAddress*
</dt> <dd>

Especifica o endereço IPv4 ou IPv6 a ser excluído da lista de escutas de IP.

</dd> </dl>

## <a name="remarks"></a>Comentários

Exclui um endereço IP para a lista de escutas de IP. Isso não inclui o número da porta. A lista de escuta de IP é usada para definir o escopo da lista de endereços aos quais o serviço HTTP associa-se. "0.0.0.0" significa qualquer endereço IPv4 e "::" significa qualquer endereço IPv6.

## <a name="examples"></a>Exemplos

**delete iplisten address=fe80::1**

**delete iplisten address=1.1.1.1**

**delete iplisten address=0.0.0.0**

**delete iplisten address=::**

 

 




