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
# <a name="add-iplisten"></a><span data-ttu-id="008e7-104">add iplisten</span><span class="sxs-lookup"><span data-stu-id="008e7-104">add iplisten</span></span>

<span data-ttu-id="008e7-105">Especifica um endereço IPv4 ou IPv6 a ser adicionado à lista de escuta de IP.</span><span class="sxs-lookup"><span data-stu-id="008e7-105">Specifies an IPv4 or IPv6 address to be added to the IP listen list.</span></span>

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="008e7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="008e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="008e7-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="008e7-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="008e7-108">Especifica o endereço IPv4 ou IPv6 a ser adicionado à lista de escuta de IP.</span><span class="sxs-lookup"><span data-stu-id="008e7-108">Specifies the IPv4 or IPv6 address to be added to the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="008e7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="008e7-109">Remarks</span></span>

<span data-ttu-id="008e7-110">Adiciona um novo endereço IP à lista de escuta de IP.</span><span class="sxs-lookup"><span data-stu-id="008e7-110">Adds a new IP address to the IP listen list.</span></span> <span data-ttu-id="008e7-111">Isso não inclui o número da porta.</span><span class="sxs-lookup"><span data-stu-id="008e7-111">This does not include the port number.</span></span> <span data-ttu-id="008e7-112">A lista de escuta de IP é usada para definir o escopo da lista de endereços aos quais o serviço HTTP associa-se.</span><span class="sxs-lookup"><span data-stu-id="008e7-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="008e7-113">"0.0.0.0" significa qualquer endereço IPv4 e "::" significa qualquer endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="008e7-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="008e7-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="008e7-114">Examples</span></span>

<span data-ttu-id="008e7-115">**add iplisten ipaddress=fe80::1**</span><span class="sxs-lookup"><span data-stu-id="008e7-115">**add iplisten ipaddress=fe80::1**</span></span>

<span data-ttu-id="008e7-116">**add iplisten ipaddress=1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="008e7-116">**add iplisten ipaddress=1.1.1.1**</span></span>

<span data-ttu-id="008e7-117">**add iplisten ipaddress=0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="008e7-117">**add iplisten ipaddress=0.0.0.0**</span></span>

<span data-ttu-id="008e7-118">**add iplisten ipaddress=::**</span><span class="sxs-lookup"><span data-stu-id="008e7-118">**add iplisten ipaddress=::**</span></span>

 

 




