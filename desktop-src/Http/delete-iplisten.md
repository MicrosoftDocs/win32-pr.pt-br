---
title: delete iplisten
description: Especifica um endereço IPv4 ou IPv6 a ser excluído da lista de escuta de IP.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- excluir HTTP iplisten
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104006773"
---
# <a name="delete-iplisten"></a>delete iplisten

Especifica um endereço IPv4 ou IPv6 a ser excluído da lista de escuta de IP.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ endereço = \]** *IPAddress*
</dt> <dd>

Especifica o endereço IPv4 ou IPv6 a ser excluído da lista de escuta de IP.

</dd> </dl>

## <a name="remarks"></a>Comentários

Exclui um endereço IP para a lista de escuta de IP. Isso não inclui o número da porta. A lista de escuta de IP é usada para definir o escopo da lista de endereços aos quais o serviço HTTP associa-se. "0.0.0.0" significa qualquer endereço IPv4 e "::" significa qualquer endereço IPv6.

## <a name="examples"></a>Exemplos

**excluir iplisten address = FE80:: 1**

**excluir iplisten address = 1.1.1.1**

**excluir endereço iplisten = 0.0.0.0**

**excluir endereço iplisten =::**

 

 




