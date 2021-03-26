---
description: Essa classe é a classe de tipo de evento para IPv4 TCP/IP conectar e aceitar eventos. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: Classe TcpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502378"
---
# <a name="tcpip_typegroup2-class"></a><span data-ttu-id="05ab1-104">\_Classe tcpip TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="05ab1-104">TcpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="05ab1-105">Essa classe é a classe de tipo de evento para IPv4 TCP/IP conectar e aceitar eventos.</span><span class="sxs-lookup"><span data-stu-id="05ab1-105">This class is the event type class for IPv4 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="05ab1-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="05ab1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="05ab1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05ab1-107">Syntax</span></span>

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
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

## <a name="members"></a><span data-ttu-id="05ab1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="05ab1-108">Members</span></span>

<span data-ttu-id="05ab1-109">A classe **tcpip \_ TypeGroup2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="05ab1-109">The **TcpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="05ab1-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05ab1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05ab1-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05ab1-111">Properties</span></span>

<span data-ttu-id="05ab1-112">A classe **tcpip \_ TypeGroup2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="05ab1-112">The **TcpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05ab1-113">**CONNID**</span><span class="sxs-lookup"><span data-stu-id="05ab1-113">**connid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05ab1-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-116">Qualificadores: **WmiDataId (15)**, **ponteiro**</span><span class="sxs-lookup"><span data-stu-id="05ab1-116">Qualifiers: **WmiDataId(15)**, **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-117">Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="05ab1-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-118">**daddr**</span><span class="sxs-lookup"><span data-stu-id="05ab1-118">**daddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="05ab1-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-121">Qualificadores: **WmiDataId (3)**, **extensão ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="05ab1-121">Qualifiers: **WmiDataId(3)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-122">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="05ab1-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-123">**dport**</span><span class="sxs-lookup"><span data-stu-id="05ab1-123">**dport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="05ab1-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-126">Qualificadores: **WmiDataId (5)**, **extensão ("porta")**</span><span class="sxs-lookup"><span data-stu-id="05ab1-126">Qualifiers: **WmiDataId(5)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-127">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="05ab1-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="05ab1-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05ab1-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-131">Qualificadores: **WmiDataId (7)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-131">Qualifiers: **WmiDataId(7)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-132">Tamanho máximo do segmento.</span><span class="sxs-lookup"><span data-stu-id="05ab1-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-133">**PESSOAL**</span><span class="sxs-lookup"><span data-stu-id="05ab1-133">**PID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05ab1-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-136">Qualificadores: **WmiDataId (1)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-136">Qualifiers: **WmiDataId(1)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-137">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="05ab1-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="05ab1-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05ab1-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-141">Qualificadores: **WmiDataId (11)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-141">Qualifiers: **WmiDataId(11)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-142">Tamanho da janela de recepção TCP.</span><span class="sxs-lookup"><span data-stu-id="05ab1-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="05ab1-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-144">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="05ab1-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-146">Qualificadores: **WmiDataId (12)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-146">Qualifiers: **WmiDataId(12)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-147">Fator de dimensionamento da janela de recepção TCP.</span><span class="sxs-lookup"><span data-stu-id="05ab1-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="05ab1-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05ab1-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-151">Qualificadores: **WmiDataId (8)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-151">Qualifiers: **WmiDataId(8)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-152">Opção SACK (confirmação seletiva) no cabeçalho TCP.</span><span class="sxs-lookup"><span data-stu-id="05ab1-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-153">**saddr**</span><span class="sxs-lookup"><span data-stu-id="05ab1-153">**saddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-154">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="05ab1-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-156">Qualificadores: **WmiDataId (4)**, **extensão ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="05ab1-156">Qualifiers: **WmiDataId(4)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-157">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="05ab1-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-158">**seqnum**</span><span class="sxs-lookup"><span data-stu-id="05ab1-158">**seqnum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05ab1-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-161">Qualificadores: **WmiDataId (14)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-161">Qualifiers: **WmiDataId(14)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-162">Número de sequência.</span><span class="sxs-lookup"><span data-stu-id="05ab1-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-163">**size**</span><span class="sxs-lookup"><span data-stu-id="05ab1-163">**size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-164">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05ab1-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-166">Qualificadores: **WmiDataId (2)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-166">Qualifiers: **WmiDataId(2)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-167">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="05ab1-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="05ab1-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-169">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="05ab1-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-171">Qualificadores: **WmiDataId (13)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-171">Qualifiers: **WmiDataId(13)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-172">Fator de dimensionamento da janela de envio TCP.</span><span class="sxs-lookup"><span data-stu-id="05ab1-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-173">**esporte**</span><span class="sxs-lookup"><span data-stu-id="05ab1-173">**sport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-174">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="05ab1-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-176">Qualificadores: **WmiDataId (6)**, **extensão ("porta")**</span><span class="sxs-lookup"><span data-stu-id="05ab1-176">Qualifiers: **WmiDataId(6)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-177">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="05ab1-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="05ab1-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-179">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05ab1-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-181">Qualificadores: **WmiDataId (9)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-181">Qualifiers: **WmiDataId(9)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-182">Opção de carimbo de data/hora no cabeçalho TCP.</span><span class="sxs-lookup"><span data-stu-id="05ab1-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="05ab1-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="05ab1-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ab1-184">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05ab1-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05ab1-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ab1-186">Qualificadores: **WmiDataId (10)**</span><span class="sxs-lookup"><span data-stu-id="05ab1-186">Qualifiers: **WmiDataId(10)**</span></span>
</dt> </dl>

<span data-ttu-id="05ab1-187">Opção de escala da janela no cabeçalho TCP.</span><span class="sxs-lookup"><span data-stu-id="05ab1-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05ab1-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05ab1-188">Requirements</span></span>



| <span data-ttu-id="05ab1-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="05ab1-189">Requirement</span></span> | <span data-ttu-id="05ab1-190">Valor</span><span class="sxs-lookup"><span data-stu-id="05ab1-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05ab1-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05ab1-191">Minimum supported client</span></span><br/> | <span data-ttu-id="05ab1-192">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05ab1-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05ab1-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05ab1-193">Minimum supported server</span></span><br/> | <span data-ttu-id="05ab1-194">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05ab1-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05ab1-195">Confira também</span><span class="sxs-lookup"><span data-stu-id="05ab1-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ab1-196">**IP**</span><span class="sxs-lookup"><span data-stu-id="05ab1-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




