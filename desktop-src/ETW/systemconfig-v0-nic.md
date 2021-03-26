---
description: Essa classe é a classe de tipo de evento para eventos de configuração de placa de interface de rede.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: Classe SystemConfig_V0_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968150"
---
# <a name="systemconfig_v0_nic-class"></a><span data-ttu-id="8751c-103">\_ \_ Classe NIC SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="8751c-103">SystemConfig\_V0\_NIC class</span></span>

<span data-ttu-id="8751c-104">Essa classe é a classe de tipo de evento para eventos de configuração de placa de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8751c-104">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="8751c-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="8751c-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8751c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8751c-106">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a><span data-ttu-id="8751c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8751c-107">Members</span></span>

<span data-ttu-id="8751c-108">A **classe \_ \_ NIC SystemConfig V0** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8751c-108">The **SystemConfig\_V0\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="8751c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8751c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8751c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8751c-110">Properties</span></span>

<span data-ttu-id="8751c-111">A **classe \_ \_ NIC SystemConfig V0** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8751c-111">The **SystemConfig\_V0\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8751c-112">**Dados**</span><span class="sxs-lookup"><span data-stu-id="8751c-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8751c-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-115">Qualificadores: **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="8751c-115">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-116">Campo de dados.</span><span class="sxs-lookup"><span data-stu-id="8751c-116">Data field.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-117">**DhcpServer**</span><span class="sxs-lookup"><span data-stu-id="8751c-117">**DhcpServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-118">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-120">Qualificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="8751c-120">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-121">Endereço IP do servidor de protocolo DHCP.</span><span class="sxs-lookup"><span data-stu-id="8751c-121">IP address of the dynamic host configuration protocol (DHCP) server.</span></span> <span data-ttu-id="8751c-122">Um valor de 255.255.255.255 indica que o servidor DHCP não pôde ser acessado ou está em processo de ser atingido.</span><span class="sxs-lookup"><span data-stu-id="8751c-122">A value of 255.255.255.255 indicates the DHCP server could not be reached, or is in the process of being reached.</span></span> <span data-ttu-id="8751c-123">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-123">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-124">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-124">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-125">**DnsServer1**</span><span class="sxs-lookup"><span data-stu-id="8751c-125">**DnsServer1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-128">Qualificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="8751c-128">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-129">Primeiro endereços IP do servidor a serem usados na consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="8751c-129">First server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="8751c-130">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-130">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-131">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-131">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-132">**DnsServer2**</span><span class="sxs-lookup"><span data-stu-id="8751c-132">**DnsServer2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-133">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-135">Qualificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="8751c-135">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-136">O segundo endereço IP do servidor a ser usado na consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="8751c-136">Second server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="8751c-137">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-137">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-138">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-138">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-139">**DnsServer3**</span><span class="sxs-lookup"><span data-stu-id="8751c-139">**DnsServer3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-140">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-142">Qualificadores: **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="8751c-142">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-143">Os endereços IP do terceiro servidor a serem usados na consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="8751c-143">Third server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="8751c-144">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-144">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-145">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-145">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-146">**DnsServer4**</span><span class="sxs-lookup"><span data-stu-id="8751c-146">**DnsServer4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-149">Qualificadores: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="8751c-149">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-150">Quarto endereço IP do servidor a ser usado na consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="8751c-150">Fourth server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="8751c-151">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-151">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-152">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-152">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-153">**Gateway**</span><span class="sxs-lookup"><span data-stu-id="8751c-153">**Gateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-154">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-156">Qualificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="8751c-156">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-157">Endereço IP do gateway padrão que o sistema de computador usa.</span><span class="sxs-lookup"><span data-stu-id="8751c-157">IP address of default gateway that the computer system uses.</span></span> <span data-ttu-id="8751c-158">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-158">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-159">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-159">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-160">**Index**</span><span class="sxs-lookup"><span data-stu-id="8751c-160">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-161">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8751c-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-163">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="8751c-163">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-164">Índice do adaptador.</span><span class="sxs-lookup"><span data-stu-id="8751c-164">Adapter index.</span></span> <span data-ttu-id="8751c-165">O índice do adaptador pode ser alterado quando um adaptador está desabilitado e, em seguida, habilitado ou em outras circunstâncias, e não deve ser considerado persistente.</span><span class="sxs-lookup"><span data-stu-id="8751c-165">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-166">**IP**</span><span class="sxs-lookup"><span data-stu-id="8751c-166">**IpAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-167">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-167">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-169">Qualificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="8751c-169">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-170">Endereços IP associados à placa de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8751c-170">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="8751c-171">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-171">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-172">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-172">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-173">**NICName**</span><span class="sxs-lookup"><span data-stu-id="8751c-173">**NICName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-174">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="8751c-174">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8751c-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-176">Qualificadores: **WmiDataId** (1), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="8751c-176">Qualifiers: **WmiDataId** (1), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-177">Nome da placa de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8751c-177">Name of the network interface card.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-178">**PhysicalAddr**</span><span class="sxs-lookup"><span data-stu-id="8751c-178">**PhysicalAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-179">Tipo de dados: **char16**</span><span class="sxs-lookup"><span data-stu-id="8751c-179">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-181">Qualificadores: **WmiDataId** (4), **máx** . (8)</span><span class="sxs-lookup"><span data-stu-id="8751c-181">Qualifiers: **WmiDataId** (4), **Max** (8)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-182">Endereço de hardware do adaptador.</span><span class="sxs-lookup"><span data-stu-id="8751c-182">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-183">**PhysicalAddrLen**</span><span class="sxs-lookup"><span data-stu-id="8751c-183">**PhysicalAddrLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-184">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8751c-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-186">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="8751c-186">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-187">Comprimento do endereço de hardware para o adaptador.</span><span class="sxs-lookup"><span data-stu-id="8751c-187">Length of the hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-188">**PrimaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="8751c-188">**PrimaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-189">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-191">Qualificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="8751c-191">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-192">Endereço IP do servidor WINS primário.</span><span class="sxs-lookup"><span data-stu-id="8751c-192">IP address for the primary WINS server.</span></span> <span data-ttu-id="8751c-193">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-193">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-194">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-194">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-195">**SecondaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="8751c-195">**SecondaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-196">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-196">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-198">Qualificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="8751c-198">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-199">Endereço IP do servidor WINS secundário.</span><span class="sxs-lookup"><span data-stu-id="8751c-199">IP address for the secondary WINS server.</span></span> <span data-ttu-id="8751c-200">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-200">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-201">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-201">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-202">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="8751c-202">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-203">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8751c-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-205">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="8751c-205">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-206">Tamanho, em bytes, da propriedade Data.</span><span class="sxs-lookup"><span data-stu-id="8751c-206">Size, in bytes, of the Data property.</span></span>

</dd> <dt>

<span data-ttu-id="8751c-207">**SubnetMask**</span><span class="sxs-lookup"><span data-stu-id="8751c-207">**SubnetMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8751c-208">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8751c-208">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8751c-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8751c-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8751c-210">Qualificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="8751c-210">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="8751c-211">Máscara de sub-rede associada à placa de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8751c-211">Subnet mask associated with the network interface card.</span></span> <span data-ttu-id="8751c-212">Cada byte de sint32 representa uma das quatro partes do endereço IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="8751c-212">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="8751c-213">O byte de ordem inferior contém o valor de P1, o próximo byte contém o valor de P2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8751c-213">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8751c-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8751c-214">Requirements</span></span>



| <span data-ttu-id="8751c-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="8751c-215">Requirement</span></span> | <span data-ttu-id="8751c-216">Valor</span><span class="sxs-lookup"><span data-stu-id="8751c-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8751c-217">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8751c-217">Minimum supported client</span></span><br/> | <span data-ttu-id="8751c-218">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8751c-218">None supported</span></span><br/>                            |
| <span data-ttu-id="8751c-219">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8751c-219">Minimum supported server</span></span><br/> | <span data-ttu-id="8751c-220">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8751c-220">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8751c-221">Confira também</span><span class="sxs-lookup"><span data-stu-id="8751c-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8751c-222">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="8751c-222">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




