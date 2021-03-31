---
title: Enumeração de CB_ADDRESS_TYPE (Cbclient. h)
description: Especifica o tipo de endereço.
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração de CB_ADDRESS_TYPE
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ecf17cea6ffc19743868b266236738839f9f917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644421"
---
# <a name="cb_address_type-enumeration"></a><span data-ttu-id="abb32-104">Enumeração de tipo de \_ endereço CB \_</span><span class="sxs-lookup"><span data-stu-id="abb32-104">CB\_ADDRESS\_TYPE enumeration</span></span>

<span data-ttu-id="abb32-105">Especifica o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="abb32-105">Specifies the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb32-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abb32-106">Syntax</span></span>


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="abb32-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="abb32-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="abb32-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**\_endereço CB \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="abb32-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB\_ADDR\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="abb32-109">O tipo de endereço é indefinido.</span><span class="sxs-lookup"><span data-stu-id="abb32-109">The address type is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="abb32-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**\_Endereço \_ IPv4 do CB**</span><span class="sxs-lookup"><span data-stu-id="abb32-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB\_ADDR\_IPv4**</span></span>
</dt> <dd>

<span data-ttu-id="abb32-111">O endereço é um endereço IPv4.</span><span class="sxs-lookup"><span data-stu-id="abb32-111">The address is an IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="abb32-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**\_IPv6 de endereço CB \_**</span><span class="sxs-lookup"><span data-stu-id="abb32-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB\_ADDR\_IPv6**</span></span>
</dt> <dd>

<span data-ttu-id="abb32-113">O endereço é um endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="abb32-113">The address is an IPv6 address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abb32-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abb32-114">Requirements</span></span>



| <span data-ttu-id="abb32-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="abb32-115">Requirement</span></span> | <span data-ttu-id="abb32-116">Valor</span><span class="sxs-lookup"><span data-stu-id="abb32-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abb32-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abb32-117">Minimum supported client</span></span><br/> | <span data-ttu-id="abb32-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="abb32-118">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="abb32-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abb32-119">Minimum supported server</span></span><br/> | <span data-ttu-id="abb32-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abb32-120">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="abb32-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="abb32-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="abb32-122"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="abb32-122"><dt>Cbclient.h</dt></span></span> </dl> |



 

 





