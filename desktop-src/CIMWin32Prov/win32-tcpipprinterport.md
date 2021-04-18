---
description: O Win32 \_ TCPIPPrinterPort&\# 32; A classe WMI representa um ponto de acesso do serviço TCP/IP.
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Classe Win32_TCPIPPrinterPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a0b0f0cb73cc60ff117399a636b0ab8542fac6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752203"
---
# <a name="win32_tcpipprinterport-class"></a><span data-ttu-id="71997-103">\_Classe Win32 TCPIPPrinterPort</span><span class="sxs-lookup"><span data-stu-id="71997-103">Win32\_TCPIPPrinterPort class</span></span>

<span data-ttu-id="71997-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ TCPIPPrinterPort do Win32** representa um ponto de acesso do serviço TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71997-104">The **Win32\_TCPIPPrinterPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a TCP/IP service access point.</span></span>

<span data-ttu-id="71997-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="71997-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="71997-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="71997-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71997-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71997-107">Syntax</span></span>

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a><span data-ttu-id="71997-108">Membros</span><span class="sxs-lookup"><span data-stu-id="71997-108">Members</span></span>

<span data-ttu-id="71997-109">A classe **Win32 \_ TCPIPPrinterPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="71997-109">The **Win32\_TCPIPPrinterPort** class has these types of members:</span></span>

-   [<span data-ttu-id="71997-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71997-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71997-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71997-111">Properties</span></span>

<span data-ttu-id="71997-112">A classe **Win32 \_ TCPIPPrinterPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="71997-112">The **Win32\_TCPIPPrinterPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71997-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="71997-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-114">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="71997-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71997-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71997-116">Se **for true**, o computador contará os bytes em um documento antes de enviá-los para a impressora e a impressora relatará o número de bytes realmente lidos.</span><span class="sxs-lookup"><span data-stu-id="71997-116">If **TRUE**, the computer counts the bytes in a document before sending them to the printer and the printer reports back the number of bytes actually read.</span></span> <span data-ttu-id="71997-117">Esse recurso é usado para diagnóstico quando bytes ausentes são detectados na saída de impressão.</span><span class="sxs-lookup"><span data-stu-id="71997-117">This capability is used for diagnostics when missing bytes are detected in the print output.</span></span>

</dd> <dt>

<span data-ttu-id="71997-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="71997-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71997-121">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="71997-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="71997-122">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="71997-122">A short textual description of the object.</span></span>

<span data-ttu-id="71997-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71997-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71997-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="71997-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71997-127">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="71997-127">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="71997-128">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="71997-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="71997-129">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="71997-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="71997-130">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="71997-130">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="71997-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="71997-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71997-134">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="71997-134">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="71997-135">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="71997-135">A textual description of the object.</span></span>

<span data-ttu-id="71997-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71997-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71997-137">**HostAddress**</span><span class="sxs-lookup"><span data-stu-id="71997-137">**HostAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71997-140">Endereço do dispositivo ou servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="71997-140">Address of the device or print server.</span></span>

</dd> <dt>

<span data-ttu-id="71997-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="71997-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-142">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71997-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71997-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71997-144">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="71997-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="71997-145">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="71997-145">Indicates when the object was installed.</span></span> <span data-ttu-id="71997-146">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="71997-146">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="71997-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71997-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71997-148">**Nome**</span><span class="sxs-lookup"><span data-stu-id="71997-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71997-151">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="71997-151">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="71997-152">Identifica exclusivamente o ponto de acesso de serviço e fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="71997-152">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="71997-153">Essa funcionalidade é descrita mais detalhadamente na propriedade Description do objeto.</span><span class="sxs-lookup"><span data-stu-id="71997-153">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="71997-154">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="71997-154">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="71997-155">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="71997-155">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-156">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71997-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71997-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71997-158">Número de portas TCP usadas pelo monitor de porta para se comunicar com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71997-158">Number of the TCP ports used by the port monitor to communicate with the device.</span></span>

</dd> <dt>

<span data-ttu-id="71997-159">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="71997-159">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71997-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71997-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71997-162">Protocolo de impressão usado.</span><span class="sxs-lookup"><span data-stu-id="71997-162">Printing protocol used.</span></span> <span data-ttu-id="71997-163">Algumas impressoras dão suporte apenas para LPR.</span><span class="sxs-lookup"><span data-stu-id="71997-163">Some printers support only LPR.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="71997-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="71997-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="71997-165">RAW</span><span class="sxs-lookup"><span data-stu-id="71997-165">RAW</span></span>

<span data-ttu-id="71997-166">Imprimindo diretamente em um dispositivo ou servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="71997-166">Printing directly to a device or print server.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="71997-167"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="71997-167"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="71997-168">LPR</span><span class="sxs-lookup"><span data-stu-id="71997-168">LPR</span></span>

<span data-ttu-id="71997-169">Protocolo herdado, que é eventualmente substituído por RAW.</span><span class="sxs-lookup"><span data-stu-id="71997-169">Legacy protocol, which is eventually replaced by RAW.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71997-170">**Fila**</span><span class="sxs-lookup"><span data-stu-id="71997-170">**Queue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71997-173">Nome da fila de impressão no servidor quando usado com o protocolo LPR.</span><span class="sxs-lookup"><span data-stu-id="71997-173">Name of the print queue on the server when used with the LPR protocol.</span></span>

</dd> <dt>

<span data-ttu-id="71997-174">**SNMPCommunity**</span><span class="sxs-lookup"><span data-stu-id="71997-174">**SNMPCommunity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71997-177">Valor de nível de segurança para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71997-177">Security level value for the device.</span></span>

<span data-ttu-id="71997-178">Exemplo: "Public"</span><span class="sxs-lookup"><span data-stu-id="71997-178">Example: "public'"</span></span>

</dd> <dt>

<span data-ttu-id="71997-179">**SNMPDevIndex**</span><span class="sxs-lookup"><span data-stu-id="71997-179">**SNMPDevIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-180">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71997-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71997-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71997-182">Número de índice SNMP deste dispositivo para o agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="71997-182">SNMP index number of this device for the SNMP agent.</span></span>

</dd> <dt>

<span data-ttu-id="71997-183">**SNMPEnabled**</span><span class="sxs-lookup"><span data-stu-id="71997-183">**SNMPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="71997-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71997-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71997-186">Se **for true**, essa impressora oferecerá suporte a [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (protocolo de gerenciamento de rede simples) e poderá fornecer informações de status avançadas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71997-186">If **TRUE**, this printer supports [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) and can provide rich status information from the device.</span></span>

</dd> <dt>

<span data-ttu-id="71997-187">**Status**</span><span class="sxs-lookup"><span data-stu-id="71997-187">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71997-190">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="71997-190">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="71997-191">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="71997-191">String that indicates the current status of the object.</span></span> <span data-ttu-id="71997-192">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="71997-192">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="71997-193">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="71997-193">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="71997-194">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="71997-194">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="71997-195">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="71997-195">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="71997-196">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="71997-196">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="71997-197">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="71997-197">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="71997-198">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71997-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="71997-199">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="71997-199">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="71997-200">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="71997-200">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="71997-201">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="71997-201">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="71997-202">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="71997-202">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71997-203">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="71997-203">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="71997-204">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="71997-204">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="71997-205">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="71997-205">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="71997-206">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="71997-206">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="71997-207">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="71997-207">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="71997-208">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="71997-208">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="71997-209">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="71997-209">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="71997-210">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="71997-210">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="71997-211">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="71997-211">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71997-212">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="71997-212">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71997-215">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="71997-215">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="71997-216">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="71997-216">The scoping system's creation class name.</span></span>

<span data-ttu-id="71997-217">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="71997-217">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="71997-218">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="71997-218">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71997-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71997-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71997-221">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="71997-221">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="71997-222">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="71997-222">The scoping system's name.</span></span>

<span data-ttu-id="71997-223">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="71997-223">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="71997-224">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="71997-224">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71997-225">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71997-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71997-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71997-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71997-227">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="71997-227">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="71997-228">Tipo de SAP, como anexado ou Redirecionado.</span><span class="sxs-lookup"><span data-stu-id="71997-228">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="71997-229">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="71997-229">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="71997-230">**Gravação** (1)</span><span class="sxs-lookup"><span data-stu-id="71997-230">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="71997-231">**Leitura** (2)</span><span class="sxs-lookup"><span data-stu-id="71997-231">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="71997-232">**Redirecionado** (4)</span><span class="sxs-lookup"><span data-stu-id="71997-232">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="71997-233">**Rede \_ Anexado** (8)</span><span class="sxs-lookup"><span data-stu-id="71997-233">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71997-234">**desconhecido** (16)</span><span class="sxs-lookup"><span data-stu-id="71997-234">**unknown** (16)</span></span>


<span data-ttu-id="71997-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="71997-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="71997-236">Comentários</span><span class="sxs-lookup"><span data-stu-id="71997-236">Remarks</span></span>

<span data-ttu-id="71997-237">A classe **Win32 \_ TCPIPPrinterPort** é derivada de [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="71997-237">The **Win32\_TCPIPPrinterPort** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="71997-238">O privilégio **SeLoadDriverPrivilege** é necessário para excluir uma instância dessa classe WMI.</span><span class="sxs-lookup"><span data-stu-id="71997-238">The **SeLoadDriverPrivilege** privilege is required to delete an instance of this WMI class.</span></span> <span data-ttu-id="71997-239">O trecho de script a seguir demonstra como estabelecer uma conexão com o WMI que usa esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="71997-239">The following script snippet demonstrates how to make a connection to WMI that uses this privilege.</span></span>

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a><span data-ttu-id="71997-240">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71997-240">Examples</span></span>

<span data-ttu-id="71997-241">O exemplo do PowerShell a seguir remove uma impressora e a porta de impressora TCPIP associada.</span><span class="sxs-lookup"><span data-stu-id="71997-241">The following PowerShell sample removes a printer and the associated TCPIP printer port.</span></span>


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a><span data-ttu-id="71997-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71997-242">Requirements</span></span>



| <span data-ttu-id="71997-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="71997-243">Requirement</span></span> | <span data-ttu-id="71997-244">Valor</span><span class="sxs-lookup"><span data-stu-id="71997-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="71997-245">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71997-245">Minimum supported client</span></span><br/> | <span data-ttu-id="71997-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71997-246">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="71997-247">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71997-247">Minimum supported server</span></span><br/> | <span data-ttu-id="71997-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71997-248">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="71997-249">Namespace</span><span class="sxs-lookup"><span data-stu-id="71997-249">Namespace</span></span><br/>                | <span data-ttu-id="71997-250">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="71997-250">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="71997-251">MOF</span><span class="sxs-lookup"><span data-stu-id="71997-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71997-252"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="71997-252"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="71997-253">DLL</span><span class="sxs-lookup"><span data-stu-id="71997-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71997-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71997-254"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="71997-255">Confira também</span><span class="sxs-lookup"><span data-stu-id="71997-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71997-256">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="71997-256">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dt>

[<span data-ttu-id="71997-257">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="71997-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
