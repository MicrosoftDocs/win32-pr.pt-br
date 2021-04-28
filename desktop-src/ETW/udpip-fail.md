---
description: Classe UdpIp_Fail-essa classe é a classe de tipo de evento para eventos de falha de TCP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: Classe UdpIp_Fail
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_Fail
- UdpIp_Fail.Proto
- UdpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: f923f26e1371d11e27bfd58bcb69c053bfb5f1a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105504"
---
# <a name="udpip_fail-class"></a><span data-ttu-id="c7c9c-104">\_Classe UdpIp Fail</span><span class="sxs-lookup"><span data-stu-id="c7c9c-104">UdpIp\_Fail class</span></span>

<span data-ttu-id="c7c9c-105">Essa classe é a classe de tipo de evento para eventos de falha de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c7c9c-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="c7c9c-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="c7c9c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c9c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7c9c-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class UdpIp_Fail : UdpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="c7c9c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c7c9c-108">Members</span></span>

<span data-ttu-id="c7c9c-109">A classe **UdpIp \_ Fail** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c7c9c-109">The **UdpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="c7c9c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7c9c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7c9c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7c9c-111">Properties</span></span>

<span data-ttu-id="c7c9c-112">A classe **UdpIp \_ Fail** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c7c9c-112">The **UdpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7c9c-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="c7c9c-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c9c-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c9c-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c9c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c9c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c9c-116">Motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="c7c9c-116">Reason for the failure.</span></span> <span data-ttu-id="c7c9c-117">Pode ser um dos seguintes códigos:</span><span class="sxs-lookup"><span data-stu-id="c7c9c-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="c7c9c-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Erro \_ do \_Recursos INsuficientes** (1)</span><span class="sxs-lookup"><span data-stu-id="c7c9c-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c7c9c-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Erro \_ do Excesso \_ de \_ endereços** (2)</span><span class="sxs-lookup"><span data-stu-id="c7c9c-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c7c9c-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Erro \_ do O endereço \_ existe** (3)</span><span class="sxs-lookup"><span data-stu-id="c7c9c-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c7c9c-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Erro \_ do \_Endereço inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="c7c9c-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c7c9c-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**Erro \_ do OUTRO** (5)</span><span class="sxs-lookup"><span data-stu-id="c7c9c-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c7c9c-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Erro \_ do O endereço de espera \_ \_ existe** (6)</span><span class="sxs-lookup"><span data-stu-id="c7c9c-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c7c9c-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="c7c9c-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c9c-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c9c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c9c-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c9c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c9c-127">Identifica o protocolo.</span><span class="sxs-lookup"><span data-stu-id="c7c9c-127">Identifies the protocol.</span></span> <span data-ttu-id="c7c9c-128">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c7c9c-128">Can be one of the following values:</span></span>



| <span data-ttu-id="c7c9c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c7c9c-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="c7c9c-130">Significado</span><span class="sxs-lookup"><span data-stu-id="c7c9c-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="c7c9c-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c7c9c-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="c7c9c-132">A família de endereços IPv4 (protocolo IP versão 4).</span><span class="sxs-lookup"><span data-stu-id="c7c9c-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="c7c9c-133"><dt>**AF \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="c7c9c-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="c7c9c-134">A família de endereços IPv6 (protocolo IP versão 6).</span><span class="sxs-lookup"><span data-stu-id="c7c9c-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7c9c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7c9c-135">Requirements</span></span>



| <span data-ttu-id="c7c9c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c9c-136">Requirement</span></span> | <span data-ttu-id="c7c9c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="c7c9c-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c7c9c-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c9c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c9c-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7c9c-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c7c9c-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c9c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c9c-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7c9c-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7c9c-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c7c9c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c9c-143">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="c7c9c-143">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




