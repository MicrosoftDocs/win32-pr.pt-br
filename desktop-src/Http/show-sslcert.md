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
# <a name="show-sslcert"></a><span data-ttu-id="3ba53-104">show sslcert</span><span class="sxs-lookup"><span data-stu-id="3ba53-104">show sslcert</span></span>

<span data-ttu-id="3ba53-105">Lista associações de certificado de servidor SSL e as políticas de certificado de cliente correspondentes para um endereço IP e porta.</span><span class="sxs-lookup"><span data-stu-id="3ba53-105">Lists SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="3ba53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ba53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ba53-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport = \] \* \* \* endereço IP: porta*</span><span class="sxs-lookup"><span data-stu-id="3ba53-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="3ba53-108">Especifica o endereço IPv4 ou IPv6 e a porta para a qual as associações de certificado SSL serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="3ba53-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be displayed.</span></span> <span data-ttu-id="3ba53-109">Não especificar um ipport lista todas as associações.</span><span class="sxs-lookup"><span data-stu-id="3ba53-109">Not specifying an ipport lists all bindings.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3ba53-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ba53-110">Examples</span></span>

<span data-ttu-id="3ba53-111">**Mostrar SSLCERT IPPORT = \[ FE80:: 1 \] : 443**</span><span class="sxs-lookup"><span data-stu-id="3ba53-111">**show sslcert ipport=\[fe80::1\]:443**</span></span>

<span data-ttu-id="3ba53-112">**show sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="3ba53-112">**show sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="3ba53-113">**show sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="3ba53-113">**show sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="3ba53-114">**Mostrar SSLCERT IPPORT = \[ ::: \] 443**</span><span class="sxs-lookup"><span data-stu-id="3ba53-114">**show sslcert ipport=\[::\]:443**</span></span>

 

 




