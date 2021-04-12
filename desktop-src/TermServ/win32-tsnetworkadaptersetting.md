---
title: Classe Win32_TSNetworkAdapterSetting
description: Define várias definições de configuração para a \_ classe de terminal do Win32, incluindo propriedades relacionadas ao adaptador de rede e o número máximo de conexões permitidas.
ms.assetid: b8a757e6-801b-4349-902e-76596b06df1f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSNetworkAdapterSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSNetworkAdapterSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting.Caption
- Win32_TSNetworkAdapterSetting.Description
- Win32_TSNetworkAdapterSetting.InstallDate
- Win32_TSNetworkAdapterSetting.Name
- Win32_TSNetworkAdapterSetting.Status
- Win32_TSNetworkAdapterSetting.TerminalName
- Win32_TSNetworkAdapterSetting.DeviceIDList
- Win32_TSNetworkAdapterSetting.MaximumConnections
- Win32_TSNetworkAdapterSetting.NetworkAdapterID
- Win32_TSNetworkAdapterSetting.NetworkAdapterLanaID
- Win32_TSNetworkAdapterSetting.NetworkAdapterList
- Win32_TSNetworkAdapterSetting.NetworkAdapterName
- Win32_TSNetworkAdapterSetting.PolicySourceMaximumConnections
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f2f2f1ac7d6bf4b1fd3fb5f5a92fc4fd5260a92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455474"
---
# <a name="win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="d1caf-105">\_Classe Win32 TSNetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="d1caf-105">Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="d1caf-106">A classe WMI **\_ TSNetworkAdapterSetting do Win32** define várias definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , incluindo propriedades relacionadas ao adaptador de rede e o número máximo de conexões permitidas.</span><span class="sxs-lookup"><span data-stu-id="d1caf-106">The **Win32\_TSNetworkAdapterSetting** WMI class defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

<span data-ttu-id="d1caf-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="d1caf-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="d1caf-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="d1caf-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1caf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1caf-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSNETWORKADAPTERSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   DeviceIDList[];
  uint32   MaximumConnections;
  string   NetworkAdapterID;
  uint32   NetworkAdapterLanaID;
  string   NetworkAdapterList[];
  string   NetworkAdapterName;
  uint32   PolicySourceMaximumConnections;
};
```

## <a name="members"></a><span data-ttu-id="d1caf-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d1caf-110">Members</span></span>

<span data-ttu-id="d1caf-111">A classe **Win32 \_ TSNetworkAdapterSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d1caf-111">The **Win32\_TSNetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d1caf-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1caf-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1caf-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1caf-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1caf-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1caf-114">Methods</span></span>

<span data-ttu-id="d1caf-115">A classe **Win32 \_ TSNetworkAdapterSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d1caf-115">The **Win32\_TSNetworkAdapterSetting** class has these methods.</span></span>



| <span data-ttu-id="d1caf-116">Método</span><span class="sxs-lookup"><span data-stu-id="d1caf-116">Method</span></span>                                                                                     | <span data-ttu-id="d1caf-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1caf-117">Description</span></span>                                                                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1caf-118">**SelectAllNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="d1caf-118">**SelectAllNetworkAdapters**</span></span>](win32-tsnetworkadaptersetting-selectallnetworkadapters.md) | <span data-ttu-id="d1caf-119">Seleciona todos os adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="d1caf-119">Selects all network adapters.</span></span><br/>                                                                 |
| [<span data-ttu-id="d1caf-120">**SelectNetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="d1caf-120">**SelectNetworkAdapterIP**</span></span>](win32-tsnetworkadaptersetting-selectnetworkadapterip.md)     | <span data-ttu-id="d1caf-121">Seleciona um adaptador de rede com base no endereço IP do adaptador.</span><span class="sxs-lookup"><span data-stu-id="d1caf-121">Selects a network adapter based on the adapter's IP address.</span></span><br/>                                  |
| [<span data-ttu-id="d1caf-122">**SetNetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="d1caf-122">**SetNetworkAdapterLanaID**</span></span>](setnetworkadapterlanaid-win32-tsnetworkadaptersetting.md)   | <span data-ttu-id="d1caf-123">Especifica o número de adaptador de rede de área local (LANA) do NetBIOS do adaptador de rede a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d1caf-123">Specifies the NetBIOS Local Area Network Adapter (LANA) number of the network adapter to set.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d1caf-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1caf-124">Properties</span></span>

<span data-ttu-id="d1caf-125">A classe **Win32 \_ TSNetworkAdapterSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1caf-125">The **Win32\_TSNetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1caf-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d1caf-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1caf-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-129">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d1caf-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-130">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="d1caf-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d1caf-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1caf-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d1caf-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1caf-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-135">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d1caf-135">Description of the object.</span></span>

<span data-ttu-id="d1caf-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1caf-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-137">**DeviceIDList**</span><span class="sxs-lookup"><span data-stu-id="d1caf-137">**DeviceIDList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-138">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1caf-138">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-140">Matriz de cadeia de caracteres de IDs de dispositivo disponíveis retornadas na ordem dos adaptadores de rede física retornados na matriz de propriedades **NetworkAdapterList** .</span><span class="sxs-lookup"><span data-stu-id="d1caf-140">String array of available device IDs returned in the order of physical network adapters returned in the **NetworkAdapterList** property array.</span></span> <span data-ttu-id="d1caf-141">O valor da ID do dispositivo é a propriedade **DeviceID** no [**Win32 \_ adaptador**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span><span class="sxs-lookup"><span data-stu-id="d1caf-141">The device ID value is the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1caf-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-143">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1caf-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-145">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="d1caf-145">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-146">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d1caf-146">The date the object was installed.</span></span> <span data-ttu-id="d1caf-147">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="d1caf-147">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d1caf-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1caf-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-149">**MaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="d1caf-149">**MaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1caf-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1caf-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-152">O número máximo de conexões permitidas.</span><span class="sxs-lookup"><span data-stu-id="d1caf-152">The maximum number of connections allowed.</span></span> <span data-ttu-id="d1caf-153">O valor **MAXINT** denota um número ilimitado de conexões.</span><span class="sxs-lookup"><span data-stu-id="d1caf-153">The value **MAXINT** denotes an unlimited number of connections.</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-154">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d1caf-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1caf-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-157">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="d1caf-157">The name of the object.</span></span>

<span data-ttu-id="d1caf-158">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1caf-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-159">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="d1caf-159">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1caf-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-162">O GUID que representa a ID do adaptador de rede a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d1caf-162">The GUID that represents the ID of the network adapter to set.</span></span> <span data-ttu-id="d1caf-163">Um **GUID** que consiste em todos os zeros denota todos os adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="d1caf-163">A **GUID** that consists of all zeros denotes all network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-164">**NetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="d1caf-164">**NetworkAdapterLanaID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1caf-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-167">O número de adaptador de rede de área local (LANA) do NetBIOS do adaptador de rede que é usado para identificar o adaptador de rede atribuído ao terminal.</span><span class="sxs-lookup"><span data-stu-id="d1caf-167">NetBIOS Local Area Network Adapter (LANA) number of the network adapter that is used to identify the network adapter assigned to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-168">**NetworkAdapterList**</span><span class="sxs-lookup"><span data-stu-id="d1caf-168">**NetworkAdapterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-169">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1caf-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-171">Matriz de cadeia de caracteres de adaptadores de rede física disponíveis e as IDs de dispositivo correspondentes.</span><span class="sxs-lookup"><span data-stu-id="d1caf-171">String array of available physical network adapters and the corresponding device IDs.</span></span> <span data-ttu-id="d1caf-172">As IDs de dispositivo são a propriedade **DeviceID** no [**Win32 \_ adaptador**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span><span class="sxs-lookup"><span data-stu-id="d1caf-172">The device IDs are the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-173">**NetworkAdapterName**</span><span class="sxs-lookup"><span data-stu-id="d1caf-173">**NetworkAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1caf-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-176">Descrição do adaptador de rede a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d1caf-176">Description of the network adapter to set.</span></span> <span data-ttu-id="d1caf-177">Esse valor está no [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span><span class="sxs-lookup"><span data-stu-id="d1caf-177">This value is in [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-178">**PolicySourceMaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="d1caf-178">**PolicySourceMaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-179">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1caf-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-181">Indica se a propriedade **MaximumConnections** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="d1caf-181">Indicates whether the **MaximumConnections** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="d1caf-182">0</span><span class="sxs-lookup"><span data-stu-id="d1caf-182">0</span></span>
</dt> <dd>

<span data-ttu-id="d1caf-183">Servidor</span><span class="sxs-lookup"><span data-stu-id="d1caf-183">Server</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-184">1</span><span class="sxs-lookup"><span data-stu-id="d1caf-184">1</span></span>
</dt> <dd>

<span data-ttu-id="d1caf-185">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="d1caf-185">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="d1caf-186">2</span><span class="sxs-lookup"><span data-stu-id="d1caf-186">2</span></span>
</dt> <dd>

<span data-ttu-id="d1caf-187">Padrão</span><span class="sxs-lookup"><span data-stu-id="d1caf-187">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1caf-188">**Status**</span><span class="sxs-lookup"><span data-stu-id="d1caf-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1caf-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-191">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="d1caf-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-192">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d1caf-192">Current status of the object.</span></span> <span data-ttu-id="d1caf-193">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="d1caf-193">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d1caf-194">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d1caf-194">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d1caf-195">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="d1caf-195">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1caf-196">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="d1caf-196">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1caf-197">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="d1caf-197">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1caf-198">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1caf-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d1caf-199">("OK")</span><span class="sxs-lookup"><span data-stu-id="d1caf-199">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1caf-200">("Erro")</span><span class="sxs-lookup"><span data-stu-id="d1caf-200">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1caf-201">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="d1caf-201">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1caf-202">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="d1caf-202">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1caf-203">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d1caf-203">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1caf-204">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="d1caf-204">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1caf-205">("Parando")</span><span class="sxs-lookup"><span data-stu-id="d1caf-205">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1caf-206">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="d1caf-206">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1caf-207">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="d1caf-207">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caf-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1caf-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1caf-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1caf-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1caf-210">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="d1caf-210">The name of the terminal.</span></span>

<span data-ttu-id="d1caf-211">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="d1caf-211">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1caf-212">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1caf-212">Remarks</span></span>

<span data-ttu-id="d1caf-213">Lembre-se de que o WinStations associado à sessão de console não pode acessar os métodos e as propriedades dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d1caf-213">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="d1caf-214">Se for feita uma tentativa de fazer isso especificando "console" como o valor da propriedade Terminalname, os métodos desse objeto retornam **WBEM \_ E \_ sem \_ suporte**.</span><span class="sxs-lookup"><span data-stu-id="d1caf-214">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="d1caf-215">Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto para adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="d1caf-215">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="d1caf-216">Para se conectar ao namespace " \\ \\ terminal cimv2" raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="d1caf-216">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="d1caf-217">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="d1caf-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="d1caf-218">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="d1caf-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="d1caf-219">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="d1caf-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="d1caf-220">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d1caf-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d1caf-221">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d1caf-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d1caf-222">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="d1caf-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d1caf-223">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d1caf-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1caf-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1caf-224">Requirements</span></span>



| <span data-ttu-id="d1caf-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1caf-225">Requirement</span></span> | <span data-ttu-id="d1caf-226">Valor</span><span class="sxs-lookup"><span data-stu-id="d1caf-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1caf-227">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1caf-227">Minimum supported client</span></span><br/> | <span data-ttu-id="d1caf-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1caf-228">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1caf-229">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1caf-229">Minimum supported server</span></span><br/> | <span data-ttu-id="d1caf-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1caf-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1caf-231">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1caf-231">Namespace</span></span><br/>                | <span data-ttu-id="d1caf-232">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="d1caf-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d1caf-233">MOF</span><span class="sxs-lookup"><span data-stu-id="d1caf-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1caf-234"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1caf-234"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1caf-235">DLL</span><span class="sxs-lookup"><span data-stu-id="d1caf-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1caf-236"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1caf-236"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1caf-237">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1caf-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1caf-238">**\_Adaptador Win32**</span><span class="sxs-lookup"><span data-stu-id="d1caf-238">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)
</dt> <dt>

[<span data-ttu-id="d1caf-239">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="d1caf-239">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
</dt> <dt>

[<span data-ttu-id="d1caf-240">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d1caf-240">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="d1caf-241">**\_TSNetworkAdapterListSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d1caf-241">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> </dl>

 

