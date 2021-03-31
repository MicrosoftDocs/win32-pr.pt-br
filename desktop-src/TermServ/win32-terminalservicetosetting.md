---
title: Classe Win32_TerminalServiceToSetting
description: Representa a associação entre uma instância da classe Win32 \_ TerminalService e a configuração de uma determinada propriedade Win32 \_ TerminalServiceSetting.
ms.assetid: 4c206812-7549-4410-b6ba-1163f20d2bee
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TerminalServiceToSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TerminalServiceToSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TerminalServiceToSetting
- Win32_TerminalServiceToSetting.Caption
- Win32_TerminalServiceToSetting.Description
- Win32_TerminalServiceToSetting.InstallDate
- Win32_TerminalServiceToSetting.Name
- Win32_TerminalServiceToSetting.Status
- Win32_TerminalServiceToSetting.Element
- Win32_TerminalServiceToSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d37a255b0a894ab257166f17c765f009d33b075
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369556"
---
# <a name="win32_terminalservicetosetting-class"></a><span data-ttu-id="cacc9-105">\_Classe Win32 TerminalServiceToSetting</span><span class="sxs-lookup"><span data-stu-id="cacc9-105">Win32\_TerminalServiceToSetting class</span></span>

<span data-ttu-id="cacc9-106">A classe WMI **\_ TerminalServiceToSetting do Win32** representa a associação entre uma instância da classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e a configuração de uma determinada propriedade [**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) .</span><span class="sxs-lookup"><span data-stu-id="cacc9-106">The **Win32\_TerminalServiceToSetting** WMI class represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span> <span data-ttu-id="cacc9-107">As definições de configuração incluem o modo de servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), licenciamento, Active Desktop, capacidade de permissões, exclusão de pastas temporárias e pastas temporárias por sessão.</span><span class="sxs-lookup"><span data-stu-id="cacc9-107">Configuration settings include Remote Desktop Session Host (RD Session Host) server mode, Licensing, Active Desktop, Permissions Capability, Deletion of Temporary Folders and Temporary Folders-Per-Session.</span></span>

<span data-ttu-id="cacc9-108">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas.</span><span class="sxs-lookup"><span data-stu-id="cacc9-108">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cacc9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cacc9-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TERMINALSERVICETOSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceToSetting : CIM_ElementSetting
{
  string                           Caption;
  string                           Description;
  datetime                         InstallDate;
  string                           Name;
  string                           Status;
  Win32_TerminalService        REF Element;
  Win32_TerminalServiceSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="cacc9-110">Membros</span><span class="sxs-lookup"><span data-stu-id="cacc9-110">Members</span></span>

<span data-ttu-id="cacc9-111">A classe **Win32 \_ TerminalServiceToSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cacc9-111">The **Win32\_TerminalServiceToSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="cacc9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cacc9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cacc9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cacc9-113">Properties</span></span>

<span data-ttu-id="cacc9-114">A classe **Win32 \_ TerminalServiceToSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cacc9-114">The **Win32\_TerminalServiceToSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cacc9-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="cacc9-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cacc9-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cacc9-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cacc9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cacc9-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cacc9-119">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="cacc9-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="cacc9-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cacc9-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cacc9-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cacc9-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cacc9-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cacc9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cacc9-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cacc9-124">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="cacc9-124">Description of the object.</span></span>

<span data-ttu-id="cacc9-125">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cacc9-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cacc9-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="cacc9-126">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cacc9-127">Tipo de dados: **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="cacc9-127">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cacc9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cacc9-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cacc9-130">Representa a instância do [**Win32 \_ TerminalService**](win32-terminalservice.md) que pode ser configurada com a propriedade **Setting** .</span><span class="sxs-lookup"><span data-stu-id="cacc9-130">Represents the instance of [**Win32\_TerminalService**](win32-terminalservice.md) that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="cacc9-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cacc9-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cacc9-132">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cacc9-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cacc9-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-134">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="cacc9-134">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="cacc9-135">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="cacc9-135">The date the object was installed.</span></span> <span data-ttu-id="cacc9-136">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="cacc9-136">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cacc9-137">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cacc9-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cacc9-138">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cacc9-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cacc9-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cacc9-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cacc9-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cacc9-141">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="cacc9-141">The name of the object.</span></span>

<span data-ttu-id="cacc9-142">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cacc9-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cacc9-143">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="cacc9-143">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cacc9-144">Tipo de dados: **Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="cacc9-144">Data type: **Win32\_TerminalServiceSetting**</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cacc9-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-146">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cacc9-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cacc9-147">Representa as definições de configuração de Serviços de Área de Trabalho Remota que podem ser aplicadas ao servidor Host da Sessão RD associado.</span><span class="sxs-lookup"><span data-stu-id="cacc9-147">Represents the Remote Desktop Services configuration settings that can be applied to the associated RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="cacc9-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="cacc9-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cacc9-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cacc9-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cacc9-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cacc9-151">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="cacc9-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="cacc9-152">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cacc9-152">Current status of the object.</span></span> <span data-ttu-id="cacc9-153">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="cacc9-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="cacc9-154">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="cacc9-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="cacc9-155">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="cacc9-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cacc9-156">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="cacc9-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cacc9-157">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="cacc9-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cacc9-158">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cacc9-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="cacc9-159">("OK")</span><span class="sxs-lookup"><span data-stu-id="cacc9-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cacc9-160">("Erro")</span><span class="sxs-lookup"><span data-stu-id="cacc9-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cacc9-161">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="cacc9-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cacc9-162">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="cacc9-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cacc9-163">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="cacc9-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cacc9-164">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="cacc9-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cacc9-165">("Parando")</span><span class="sxs-lookup"><span data-stu-id="cacc9-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cacc9-166">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="cacc9-166">("Service")</span></span>


<span data-ttu-id="cacc9-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cacc9-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="cacc9-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="cacc9-168">Remarks</span></span>

<span data-ttu-id="cacc9-169">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cacc9-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cacc9-170">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cacc9-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cacc9-171">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="cacc9-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cacc9-172">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cacc9-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cacc9-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cacc9-173">Requirements</span></span>



| <span data-ttu-id="cacc9-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="cacc9-174">Requirement</span></span> | <span data-ttu-id="cacc9-175">Valor</span><span class="sxs-lookup"><span data-stu-id="cacc9-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cacc9-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cacc9-176">Minimum supported client</span></span><br/> | <span data-ttu-id="cacc9-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cacc9-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cacc9-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cacc9-178">Minimum supported server</span></span><br/> | <span data-ttu-id="cacc9-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cacc9-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cacc9-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="cacc9-180">Namespace</span></span><br/>                | <span data-ttu-id="cacc9-181">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="cacc9-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cacc9-182">MOF</span><span class="sxs-lookup"><span data-stu-id="cacc9-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cacc9-183"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cacc9-183"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cacc9-184">DLL</span><span class="sxs-lookup"><span data-stu-id="cacc9-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cacc9-185"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cacc9-185"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cacc9-186">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cacc9-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cacc9-187">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="cacc9-187">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="cacc9-188">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="cacc9-188">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="cacc9-189">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cacc9-189">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="cacc9-190">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="cacc9-190">**CIM\_ElementSetting**</span></span>](/windows/desktop/CIMWin32Prov/cim-elementsetting)
</dt> </dl>

 

