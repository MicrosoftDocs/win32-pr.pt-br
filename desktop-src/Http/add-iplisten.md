---
title: add iplisten
description: Especifica um endereço IPv4 ou IPv6 a ser adicionado à lista de escuta de IP.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- Adicionar HTTP iplisten
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "103917043"
---
# <a name="add-iplisten"></a>add iplisten

Especifica um endereço IPv4 ou IPv6 a ser adicionado à lista de escuta de IP.

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*
</dt> <dd>

Especifica o endereço IPv4 ou IPv6 a ser adicionado à lista de escuta de IP.

</dd> </dl>

## <a name="remarks"></a>Comentários

Adiciona um novo endereço IP à lista de escuta de IP. Isso não inclui o número da porta. A lista de escuta de IP é usada para definir o escopo da lista de endereços aos quais o serviço HTTP associa-se. "0.0.0.0" significa qualquer endereço IPv4 e "::" significa qualquer endereço IPv6.

## <a name="examples"></a>Exemplos

**add iplisten ipaddress=fe80::1**

**add iplisten ipaddress=1.1.1.1**

**add iplisten ipaddress=0.0.0.0**

**add iplisten ipaddress=::**

 

 




