---
title: Classe Win32_TSVirtualIP
description: Define as configurações de virtualização de IP (Internet Protocol) para um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSVirtualIP Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSVirtualIP classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f87db04d61dda0c6034b536544362ec09e0aaa66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644320"
---
# <a name="win32_tsvirtualip-class"></a><span data-ttu-id="9c0d8-105">\_Classe Win32 TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="9c0d8-105">Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="9c0d8-106">Define as configurações de virtualização de IP (Internet Protocol) para um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="9c0d8-106">Defines Internet protocol (IP) virtualization settings for a Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="9c0d8-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c0d8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c0d8-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a><span data-ttu-id="9c0d8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="9c0d8-109">Members</span></span>

<span data-ttu-id="9c0d8-110">A classe **Win32 \_ TSVirtualIP** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9c0d8-110">The **Win32\_TSVirtualIP** class has these types of members:</span></span>

-   [<span data-ttu-id="9c0d8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c0d8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c0d8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9c0d8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c0d8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c0d8-113">Methods</span></span>

<span data-ttu-id="9c0d8-114">A classe **Win32 \_ TSVirtualIP** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-114">The **Win32\_TSVirtualIP** class has these methods.</span></span>



| <span data-ttu-id="9c0d8-115">Método</span><span class="sxs-lookup"><span data-stu-id="9c0d8-115">Method</span></span>                                                                                                   | <span data-ttu-id="9c0d8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c0d8-116">Description</span></span>                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c0d8-117">**Addprogram**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-117">**AddProgram**</span></span>](addprogram-win32-tsvirtualip.md)                                                       | <span data-ttu-id="9c0d8-118">Adiciona um programa à lista de programas que usam a virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-118">Adds a program to the list of programs that use IP virtualization.</span></span><br/>                                                                                                |
| [<span data-ttu-id="9c0d8-119">**RemoveProgram**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-119">**RemoveProgram**</span></span>](removeprogram-win32-tsvirtualip.md)                                                 | <span data-ttu-id="9c0d8-120">Remove um programa da lista de programas que usam a virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-120">Removes a program from the list of programs that use IP virtualization.</span></span><br/>                                                                                           |
| [<span data-ttu-id="9c0d8-121">**SelectNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-121">**SelectNetworkAdapter**</span></span>](selectnetworkadapter-win32-tsvirtualip.md)                                   | <span data-ttu-id="9c0d8-122">Define o endereço MAC do adaptador de rede a ser usado para virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-122">Sets the MAC address of the network adapter to use for IP virtualization.</span></span><br/>                                                                                         |
| [<span data-ttu-id="9c0d8-123">**Setprogramlist**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-123">**SetProgramList**</span></span>](setprogramlist-win32-tsvirtualip.md)                                               | <span data-ttu-id="9c0d8-124">Substitui a lista de programas que usam a virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-124">Overwrites the list of programs that use IP virtualization.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="9c0d8-125">**SetVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-125">**SetVirtualIPActive**</span></span>](setvirtualipactive-win32-tsvirtualip.md)                                       | <span data-ttu-id="9c0d8-126">Define o valor da propriedade **VirtualIPActive** .</span><span class="sxs-lookup"><span data-stu-id="9c0d8-126">Sets the **VirtualIPActive** property value.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="9c0d8-127">**SetVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-127">**SetVirtualIPMode**</span></span>](setvirtualipmode-win32-tsvirtualip.md)                                           | <span data-ttu-id="9c0d8-128">Define o valor da propriedade **VirtualIPMode** .</span><span class="sxs-lookup"><span data-stu-id="9c0d8-128">Sets the **VirtualIPMode** property value.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="9c0d8-129">**SetVirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-129">**SetVirtualizeLoopbackAddressesEnabled**</span></span>](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | <span data-ttu-id="9c0d8-130">Define o valor da propriedade **VirtualizeLoopbackAddressesEnabled** .</span><span class="sxs-lookup"><span data-stu-id="9c0d8-130">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span><br/> <span data-ttu-id="9c0d8-131">**Windows Server 2008 R2:** Esse método não está disponível antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-131">**Windows Server 2008 R2:** This method is not available prior to Windows Server 2012.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9c0d8-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9c0d8-132">Properties</span></span>

<span data-ttu-id="9c0d8-133">A classe **Win32 \_ TSVirtualIP** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-133">The **Win32\_TSVirtualIP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c0d8-134">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-137">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-138">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-138">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="9c0d8-139">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c0d8-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-140">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-143">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-143">Description of the object.</span></span>

<span data-ttu-id="9c0d8-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c0d8-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-146">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-148">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="9c0d8-148">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-149">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-149">The date the object was installed.</span></span> <span data-ttu-id="9c0d8-150">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-150">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9c0d8-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c0d8-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-155">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-155">The name of the object.</span></span>

<span data-ttu-id="9c0d8-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c0d8-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-157">**NetworkAdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-157">**NetworkAdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-160">A descrição do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-160">The description for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-161">**NetworkAdapterDescriptionList**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-161">**NetworkAdapterDescriptionList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-162">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-162">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-164">A lista de descrições dos adaptadores de rede física disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-164">The list of descriptions of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-165">**NetworkAdapterMacAddress**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-165">**NetworkAdapterMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-168">O endereço MAC do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-168">The MAC address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-169">**NetworkAdapterMacList**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-169">**NetworkAdapterMacList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-170">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-172">A lista de endereços MAC dos adaptadores de rede física disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-172">The list of MAC addresses of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-173">**PolicySourceNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-173">**PolicySourceNetworkAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-174">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-176">Indica se o adaptador de rede está configurado pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-176">Indicates whether the network adapter is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="9c0d8-177">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-177">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="9c0d8-178">Servidor</span><span class="sxs-lookup"><span data-stu-id="9c0d8-178">Server</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-179">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-179">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9c0d8-180">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="9c0d8-180">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c0d8-181">**PolicySourceProgramList**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-181">**PolicySourceProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-182">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-184">Indica se a propriedade **programlist** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-184">Indicates whether the **ProgramList** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="9c0d8-185">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-185">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="9c0d8-186">Servidor</span><span class="sxs-lookup"><span data-stu-id="9c0d8-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-187">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-187">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9c0d8-188">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="9c0d8-188">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c0d8-189">**PolicySourceVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-189">**PolicySourceVirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-190">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-192">Indica se a propriedade **VirtualIPActive** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-192">Indicates if the **VirtualIPActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="9c0d8-193">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-193">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="9c0d8-194">Servidor</span><span class="sxs-lookup"><span data-stu-id="9c0d8-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-195">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-195">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9c0d8-196">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="9c0d8-196">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c0d8-197">**PolicySourceVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-197">**PolicySourceVirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-198">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-200">Indica se a propriedade **VirtualIPMode** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-200">Indicates if the **VirtualIPMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="9c0d8-201">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-201">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="9c0d8-202">Servidor</span><span class="sxs-lookup"><span data-stu-id="9c0d8-202">Server</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-203">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-203">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9c0d8-204">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="9c0d8-204">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c0d8-205">**Programalist**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-205">**ProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-206">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-208">Especifica os programas que são configurados para usar a virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-208">Specifies the programs that are configured to use IP virtualization.</span></span> <span data-ttu-id="9c0d8-209">Isso pode ser um nome de programa ou o caminho completo.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-209">This may a program name or the full path.</span></span>

</dd> <dt>

<span data-ttu-id="9c0d8-210">**Status**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-210">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-213">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-214">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-214">Current status of the object.</span></span> <span data-ttu-id="9c0d8-215">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-215">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9c0d8-216">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="9c0d8-216">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9c0d8-217">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="9c0d8-217">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9c0d8-218">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-218">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9c0d8-219">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-219">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9c0d8-220">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c0d8-220">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="9c0d8-221">("OK")</span><span class="sxs-lookup"><span data-stu-id="9c0d8-221">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9c0d8-222">("Erro")</span><span class="sxs-lookup"><span data-stu-id="9c0d8-222">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9c0d8-223">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="9c0d8-223">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9c0d8-224">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="9c0d8-224">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9c0d8-225">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9c0d8-225">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9c0d8-226">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="9c0d8-226">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9c0d8-227">("Parando")</span><span class="sxs-lookup"><span data-stu-id="9c0d8-227">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9c0d8-228">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="9c0d8-228">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9c0d8-229">**VirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-229">**VirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-230">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-232">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-232">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-233">Especifica se a virtualização de IP está ativa no servidor.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-233">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="9c0d8-234">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-234">This can be one of the following values.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="9c0d8-235"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-235"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9c0d8-236">A virtualização de IP não está ativa.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-236">IP virtualization is not active.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="9c0d8-237"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-237"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9c0d8-238">A virtualização de IP está ativa.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-238">IP virtualization is active.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c0d8-239">**VirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-239">**VirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-240">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-242">Especifica qual modo de virtualização de IP está sendo usado no servidor.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-242">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="9c0d8-243">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-243">This can be one of the following values.</span></span>

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span data-ttu-id="9c0d8-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Por sessão** (0)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Per-Session** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9c0d8-245">O modo de virtualização de IP é por sessão.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-245">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span data-ttu-id="9c0d8-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Por programa** (1)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Per-Program** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9c0d8-247">O modo de virtualização de IP é por usuário.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-247">The IP virtualization mode is per-user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c0d8-248">**VirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-248">**VirtualizeLoopbackAddressesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0d8-249">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c0d8-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0d8-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c0d8-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0d8-251">Especifica se a virtualização de endereço de loopback está habilitada.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-251">Specifies whether loopback address virtualization is enabled.</span></span>

<span data-ttu-id="9c0d8-252">**Windows Server 2008 R2:** Essa propriedade não está disponível antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-252">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="9c0d8-253"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-253"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9c0d8-254">não ativado</span><span class="sxs-lookup"><span data-stu-id="9c0d8-254">Not enabled</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="9c0d8-255"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="9c0d8-255"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9c0d8-256">habilitado</span><span class="sxs-lookup"><span data-stu-id="9c0d8-256">Enabled</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c0d8-257">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c0d8-257">Remarks</span></span>

<span data-ttu-id="9c0d8-258">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9c0d8-258">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9c0d8-259">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-259">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9c0d8-260">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9c0d8-260">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9c0d8-261">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9c0d8-261">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c0d8-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c0d8-262">Requirements</span></span>



| <span data-ttu-id="9c0d8-263">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c0d8-263">Requirement</span></span> | <span data-ttu-id="9c0d8-264">Valor</span><span class="sxs-lookup"><span data-stu-id="9c0d8-264">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0d8-265">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c0d8-265">Minimum supported client</span></span><br/> | <span data-ttu-id="9c0d8-266">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9c0d8-266">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9c0d8-267">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c0d8-267">Minimum supported server</span></span><br/> | <span data-ttu-id="9c0d8-268">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c0d8-268">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="9c0d8-269">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c0d8-269">Namespace</span></span><br/>                | <span data-ttu-id="9c0d8-270">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9c0d8-270">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9c0d8-271">MOF</span><span class="sxs-lookup"><span data-stu-id="9c0d8-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c0d8-272"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c0d8-272"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c0d8-273">DLL</span><span class="sxs-lookup"><span data-stu-id="9c0d8-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c0d8-274"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c0d8-274"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

