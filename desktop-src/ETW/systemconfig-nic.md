---
description: Essa classe é a classe de tipo de evento para eventos de configuração de placa de interface de rede. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: Classe SystemConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920942"
---
# <a name="systemconfig_nic-class"></a><span data-ttu-id="dfa3f-104">\_Classe NIC SystemConfig</span><span class="sxs-lookup"><span data-stu-id="dfa3f-104">SystemConfig\_NIC class</span></span>

<span data-ttu-id="dfa3f-105">Essa classe é a classe de tipo de evento para eventos de configuração de placa de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-105">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="dfa3f-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa3f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfa3f-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a><span data-ttu-id="dfa3f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="dfa3f-108">Members</span></span>

<span data-ttu-id="dfa3f-109">A **classe \_ NIC SystemConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dfa3f-109">The **SystemConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="dfa3f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dfa3f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfa3f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dfa3f-111">Properties</span></span>

<span data-ttu-id="dfa3f-112">A **classe \_ NIC SystemConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-112">The **SystemConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfa3f-113">DnsServerAddresses</span><span class="sxs-lookup"><span data-stu-id="dfa3f-113">DnsServerAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa3f-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dfa3f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dfa3f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-116">Qualificadores: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="dfa3f-116">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="dfa3f-117">Endereços IP a serem usados na consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-117">IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="dfa3f-118">A lista de endereços é delimitada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-118">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="dfa3f-119">IpAddresses</span><span class="sxs-lookup"><span data-stu-id="dfa3f-119">IpAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa3f-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dfa3f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dfa3f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-122">Qualificadores: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="dfa3f-122">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="dfa3f-123">Endereços IP associados à placa de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-123">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="dfa3f-124">A lista de endereços é delimitada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-124">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="dfa3f-125">Ipv4Index</span><span class="sxs-lookup"><span data-stu-id="dfa3f-125">Ipv4Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa3f-126">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfa3f-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dfa3f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-128">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="dfa3f-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="dfa3f-129">Índice de adaptador para NIC IPv4.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-129">Adapter index for IPv4 NIC.</span></span> <span data-ttu-id="dfa3f-130">O índice do adaptador pode ser alterado quando um adaptador está desabilitado e, em seguida, habilitado ou em outras circunstâncias, e não deve ser considerado persistente.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-130">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="dfa3f-131">Ipv6Index</span><span class="sxs-lookup"><span data-stu-id="dfa3f-131">Ipv6Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa3f-132">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfa3f-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dfa3f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-134">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="dfa3f-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="dfa3f-135">Índice de adaptador para NIC IPv6.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-135">Adapter index for IPv6 NIC.</span></span> <span data-ttu-id="dfa3f-136">O índice do adaptador pode ser alterado quando um adaptador está desabilitado e, em seguida, habilitado ou em outras circunstâncias, e não deve ser considerado persistente.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-136">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="dfa3f-137">NICDescription</span><span class="sxs-lookup"><span data-stu-id="dfa3f-137">NICDescription</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa3f-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dfa3f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dfa3f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-140">Qualificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="dfa3f-140">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="dfa3f-141">Descrição do adaptador.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-141">Description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dfa3f-142">PhysicalAddr</span><span class="sxs-lookup"><span data-stu-id="dfa3f-142">PhysicalAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa3f-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dfa3f-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dfa3f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-145">Qualificadores: WmiDataId (1), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="dfa3f-145">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="dfa3f-146">Endereço de hardware do adaptador.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-146">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dfa3f-147">PhysicalAddrLen</span><span class="sxs-lookup"><span data-stu-id="dfa3f-147">PhysicalAddrLen</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa3f-148">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfa3f-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dfa3f-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa3f-150">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="dfa3f-150">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="dfa3f-151">Comprimento do endereço de hardware para o adaptador.</span><span class="sxs-lookup"><span data-stu-id="dfa3f-151">Length of the hardware address for the adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfa3f-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfa3f-152">Requirements</span></span>



| <span data-ttu-id="dfa3f-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfa3f-153">Requirement</span></span> | <span data-ttu-id="dfa3f-154">Valor</span><span class="sxs-lookup"><span data-stu-id="dfa3f-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dfa3f-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfa3f-155">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa3f-156">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfa3f-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dfa3f-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfa3f-157">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa3f-158">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dfa3f-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dfa3f-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfa3f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa3f-160">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="dfa3f-160">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




