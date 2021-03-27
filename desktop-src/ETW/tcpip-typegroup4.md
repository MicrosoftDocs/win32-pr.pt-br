---
description: Essa classe é a classe de tipo de evento para IPv6 TCP/IP Connect e aceita eventos. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: c6c0463a-0058-47cf-9235-d2b621f30fb4
title: Classe TcpIp_TypeGroup4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup4
- TcpIp_TypeGroup4.PID
- TcpIp_TypeGroup4.size
- TcpIp_TypeGroup4.daddr
- TcpIp_TypeGroup4.saddr
- TcpIp_TypeGroup4.dport
- TcpIp_TypeGroup4.sport
- TcpIp_TypeGroup4.mss
- TcpIp_TypeGroup4.sackopt
- TcpIp_TypeGroup4.tsopt
- TcpIp_TypeGroup4.wsopt
- TcpIp_TypeGroup4.rcvwin
- TcpIp_TypeGroup4.rcvwinscale
- TcpIp_TypeGroup4.sndwinscale
- TcpIp_TypeGroup4.seqnum
- TcpIp_TypeGroup4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 942e5897db6771c0c3a9df965e5e889eaf71c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661569"
---
# <a name="tcpip_typegroup4-class"></a><span data-ttu-id="43f94-104">\_Classe tcpip TypeGroup4</span><span class="sxs-lookup"><span data-stu-id="43f94-104">TcpIp\_TypeGroup4 class</span></span>

<span data-ttu-id="43f94-105">Essa classe é a classe de tipo de evento para IPv6 TCP/IP Connect e aceita eventos.</span><span class="sxs-lookup"><span data-stu-id="43f94-105">This class is the event type class for IPv6 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="43f94-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="43f94-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f94-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43f94-107">Syntax</span></span>

``` syntax
[EventType{28, 31}, EventTypeName{"ConnectIPV6", "AcceptIPV6"}]
class TcpIp_TypeGroup4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="43f94-108">Membros</span><span class="sxs-lookup"><span data-stu-id="43f94-108">Members</span></span>

<span data-ttu-id="43f94-109">A classe **tcpip \_ TypeGroup4** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="43f94-109">The **TcpIp\_TypeGroup4** class has these types of members:</span></span>

-   [<span data-ttu-id="43f94-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43f94-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43f94-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43f94-111">Properties</span></span>

<span data-ttu-id="43f94-112">A classe **tcpip \_ TypeGroup4** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="43f94-112">The **TcpIp\_TypeGroup4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43f94-113">CONNID</span><span class="sxs-lookup"><span data-stu-id="43f94-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f94-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-116">Qualificadores: WmiDataId (15), ponteiro</span><span class="sxs-lookup"><span data-stu-id="43f94-116">Qualifiers: WmiDataId(15), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="43f94-117">Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="43f94-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-118">daddr</span><span class="sxs-lookup"><span data-stu-id="43f94-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="43f94-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-121">Qualificadores: WmiDataId (3), extensão ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="43f94-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="43f94-122">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="43f94-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-123">dport</span><span class="sxs-lookup"><span data-stu-id="43f94-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="43f94-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-126">Qualificadores: WmiDataId (5), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="43f94-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="43f94-127">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="43f94-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="43f94-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f94-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-131">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="43f94-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-132">Tamanho máximo do segmento.</span><span class="sxs-lookup"><span data-stu-id="43f94-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-133">PID</span><span class="sxs-lookup"><span data-stu-id="43f94-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f94-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-136">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="43f94-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-137">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="43f94-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="43f94-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f94-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-141">Qualificadores: WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="43f94-141">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-142">Tamanho da janela de recepção TCP.</span><span class="sxs-lookup"><span data-stu-id="43f94-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="43f94-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-144">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="43f94-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-146">Qualificadores: WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="43f94-146">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-147">Fator de dimensionamento da janela de recepção TCP.</span><span class="sxs-lookup"><span data-stu-id="43f94-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="43f94-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f94-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-151">Qualificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="43f94-151">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-152">Opção SACK (confirmação seletiva) no cabeçalho TCP.</span><span class="sxs-lookup"><span data-stu-id="43f94-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-153">saddr</span><span class="sxs-lookup"><span data-stu-id="43f94-153">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-154">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="43f94-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-156">Qualificadores: WmiDataId (4), extensão ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="43f94-156">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="43f94-157">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="43f94-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-158">seqnum</span><span class="sxs-lookup"><span data-stu-id="43f94-158">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f94-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-161">Qualificadores: WmiDataId (14)</span><span class="sxs-lookup"><span data-stu-id="43f94-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-162">Número de sequência.</span><span class="sxs-lookup"><span data-stu-id="43f94-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-163">tamanho</span><span class="sxs-lookup"><span data-stu-id="43f94-163">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-164">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43f94-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-166">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="43f94-166">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-167">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="43f94-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="43f94-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-169">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="43f94-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-171">Qualificadores: WmiDataId (13)</span><span class="sxs-lookup"><span data-stu-id="43f94-171">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-172">Fator de dimensionamento da janela de envio TCP.</span><span class="sxs-lookup"><span data-stu-id="43f94-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-173">esporte</span><span class="sxs-lookup"><span data-stu-id="43f94-173">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-174">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="43f94-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-176">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="43f94-176">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="43f94-177">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="43f94-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="43f94-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-179">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f94-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-181">Qualificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="43f94-181">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-182">Opção de carimbo de data/hora no cabeçalho TCP.</span><span class="sxs-lookup"><span data-stu-id="43f94-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="43f94-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="43f94-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f94-184">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43f94-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f94-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43f94-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f94-186">Qualificadores: WmiDataId (10)</span><span class="sxs-lookup"><span data-stu-id="43f94-186">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="43f94-187">Opção de escala da janela no cabeçalho TCP.</span><span class="sxs-lookup"><span data-stu-id="43f94-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43f94-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43f94-188">Requirements</span></span>



| <span data-ttu-id="43f94-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="43f94-189">Requirement</span></span> | <span data-ttu-id="43f94-190">Valor</span><span class="sxs-lookup"><span data-stu-id="43f94-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43f94-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43f94-191">Minimum supported client</span></span><br/> | <span data-ttu-id="43f94-192">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43f94-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="43f94-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43f94-193">Minimum supported server</span></span><br/> | <span data-ttu-id="43f94-194">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43f94-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43f94-195">Confira também</span><span class="sxs-lookup"><span data-stu-id="43f94-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f94-196">**IP**</span><span class="sxs-lookup"><span data-stu-id="43f94-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




