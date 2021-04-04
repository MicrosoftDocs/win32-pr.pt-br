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
# <a name="delete-iplisten"></a><span data-ttu-id="3bdbf-104">delete iplisten</span><span class="sxs-lookup"><span data-stu-id="3bdbf-104">delete iplisten</span></span>

<span data-ttu-id="3bdbf-105">Especifica um endereço IPv4 ou IPv6 a ser excluído da lista de escuta de IP.</span><span class="sxs-lookup"><span data-stu-id="3bdbf-105">Specifies an IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="3bdbf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bdbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bdbf-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ endereço = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="3bdbf-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[address=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="3bdbf-108">Especifica o endereço IPv4 ou IPv6 a ser excluído da lista de escuta de IP.</span><span class="sxs-lookup"><span data-stu-id="3bdbf-108">Specifies the IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bdbf-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bdbf-109">Remarks</span></span>

<span data-ttu-id="3bdbf-110">Exclui um endereço IP para a lista de escuta de IP.</span><span class="sxs-lookup"><span data-stu-id="3bdbf-110">Deletes an IP address to the IP listen list.</span></span> <span data-ttu-id="3bdbf-111">Isso não inclui o número da porta.</span><span class="sxs-lookup"><span data-stu-id="3bdbf-111">This does not include the port number.</span></span> <span data-ttu-id="3bdbf-112">A lista de escuta de IP é usada para definir o escopo da lista de endereços aos quais o serviço HTTP associa-se.</span><span class="sxs-lookup"><span data-stu-id="3bdbf-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="3bdbf-113">"0.0.0.0" significa qualquer endereço IPv4 e "::" significa qualquer endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="3bdbf-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="3bdbf-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3bdbf-114">Examples</span></span>

<span data-ttu-id="3bdbf-115">**excluir iplisten address = FE80:: 1**</span><span class="sxs-lookup"><span data-stu-id="3bdbf-115">**delete iplisten address=fe80::1**</span></span>

<span data-ttu-id="3bdbf-116">**excluir iplisten address = 1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="3bdbf-116">**delete iplisten address=1.1.1.1**</span></span>

<span data-ttu-id="3bdbf-117">**excluir endereço iplisten = 0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="3bdbf-117">**delete iplisten address=0.0.0.0**</span></span>

<span data-ttu-id="3bdbf-118">**excluir endereço iplisten =::**</span><span class="sxs-lookup"><span data-stu-id="3bdbf-118">**delete iplisten address=::**</span></span>

 

 




