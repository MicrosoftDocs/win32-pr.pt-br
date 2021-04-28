---
description: Classe TcpIp_Fail-essa classe é a classe de tipo de evento para eventos de falha de TCP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: Classe TcpIp_Fail
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 897c42a1c2530d3e41d1f937d5d59356a2913e2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105844"
---
# <a name="tcpip_fail-class"></a><span data-ttu-id="03ccb-104">Classe de falha de TcpIp \_</span><span class="sxs-lookup"><span data-stu-id="03ccb-104">TcpIp\_Fail class</span></span>

<span data-ttu-id="03ccb-105">Essa classe é a classe de tipo de evento para eventos de falha de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="03ccb-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="03ccb-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="03ccb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ccb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03ccb-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="03ccb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="03ccb-108">Members</span></span>

<span data-ttu-id="03ccb-109">A classe **tcpip \_ Fail** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="03ccb-109">The **TcpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="03ccb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03ccb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03ccb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03ccb-111">Properties</span></span>

<span data-ttu-id="03ccb-112">A classe **tcpip \_ Fail** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="03ccb-112">The **TcpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03ccb-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="03ccb-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ccb-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03ccb-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03ccb-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03ccb-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03ccb-116">Motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="03ccb-116">Reason for the failure.</span></span> <span data-ttu-id="03ccb-117">Pode ser um dos seguintes códigos:</span><span class="sxs-lookup"><span data-stu-id="03ccb-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="03ccb-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Erro \_ do \_Recursos INsuficientes** (1)</span><span class="sxs-lookup"><span data-stu-id="03ccb-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="03ccb-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Erro \_ do Excesso \_ de \_ endereços** (2)</span><span class="sxs-lookup"><span data-stu-id="03ccb-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="03ccb-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Erro \_ do O endereço \_ existe** (3)</span><span class="sxs-lookup"><span data-stu-id="03ccb-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="03ccb-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Erro \_ do \_Endereço inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="03ccb-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="03ccb-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**Erro \_ do OUTRO** (5)</span><span class="sxs-lookup"><span data-stu-id="03ccb-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="03ccb-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Erro \_ do O endereço de espera \_ \_ existe** (6)</span><span class="sxs-lookup"><span data-stu-id="03ccb-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="03ccb-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="03ccb-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03ccb-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03ccb-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03ccb-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03ccb-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03ccb-127">Identifica o protocolo.</span><span class="sxs-lookup"><span data-stu-id="03ccb-127">Identifies the protocol.</span></span> <span data-ttu-id="03ccb-128">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="03ccb-128">Can be one of the following values:</span></span>



| <span data-ttu-id="03ccb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="03ccb-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="03ccb-130">Significado</span><span class="sxs-lookup"><span data-stu-id="03ccb-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="03ccb-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="03ccb-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="03ccb-132">A família de endereços IPv4 (protocolo IP versão 4).</span><span class="sxs-lookup"><span data-stu-id="03ccb-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="03ccb-133"><dt>**AF \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="03ccb-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="03ccb-134">A família de endereços IPv6 (protocolo IP versão 6).</span><span class="sxs-lookup"><span data-stu-id="03ccb-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03ccb-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03ccb-135">Requirements</span></span>



| <span data-ttu-id="03ccb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="03ccb-136">Requirement</span></span> | <span data-ttu-id="03ccb-137">Valor</span><span class="sxs-lookup"><span data-stu-id="03ccb-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="03ccb-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03ccb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="03ccb-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03ccb-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="03ccb-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03ccb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="03ccb-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="03ccb-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03ccb-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="03ccb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ccb-143">**IP**</span><span class="sxs-lookup"><span data-stu-id="03ccb-143">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




