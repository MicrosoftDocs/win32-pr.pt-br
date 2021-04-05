---
title: Classe Win32_TSSessionDirectorySetting
description: Representa a associação entre uma instância da classe Win32 \_ TerminalService e uma instância da \_ classe Win32 TSSessionDirectory.
ms.assetid: b6350f7b-386f-4f6b-8ab1-29d5d21fae02
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSSessionDirectorySetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSSessionDirectorySetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectorySetting
- Win32_TSSessionDirectorySetting.Caption
- Win32_TSSessionDirectorySetting.Description
- Win32_TSSessionDirectorySetting.InstallDate
- Win32_TSSessionDirectorySetting.Name
- Win32_TSSessionDirectorySetting.Status
- Win32_TSSessionDirectorySetting.Element
- Win32_TSSessionDirectorySetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 667f501ff850cb7ee8c40448de11c06898ab8a85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008956"
---
# <a name="win32_tssessiondirectorysetting-class"></a><span data-ttu-id="8fa83-105">\_Classe Win32 TSSessionDirectorySetting</span><span class="sxs-lookup"><span data-stu-id="8fa83-105">Win32\_TSSessionDirectorySetting class</span></span>

<span data-ttu-id="8fa83-106">Representa a associação entre uma instância da classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e uma instância da classe [**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="8fa83-106">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

<span data-ttu-id="8fa83-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="8fa83-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa83-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fa83-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSSESSIONDIRECTORYSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectorySetting : CIM_ElementSetting
{
  string                       Caption;
  string                       Description;
  datetime                     InstallDate;
  string                       Name;
  string                       Status;
  Win32_TerminalService    REF Element;
  Win32_TSSessionDirectory REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="8fa83-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8fa83-109">Members</span></span>

<span data-ttu-id="8fa83-110">A classe **Win32 \_ TSSessionDirectorySetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8fa83-110">The **Win32\_TSSessionDirectorySetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8fa83-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8fa83-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fa83-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8fa83-112">Properties</span></span>

<span data-ttu-id="8fa83-113">A classe **Win32 \_ TSSessionDirectorySetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8fa83-113">The **Win32\_TSSessionDirectorySetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fa83-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8fa83-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fa83-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8fa83-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8fa83-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8fa83-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8fa83-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="8fa83-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8fa83-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fa83-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fa83-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8fa83-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fa83-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8fa83-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8fa83-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fa83-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8fa83-123">Description of the object.</span></span>

<span data-ttu-id="8fa83-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fa83-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fa83-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="8fa83-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fa83-126">Tipo de dados: **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="8fa83-126">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8fa83-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fa83-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fa83-129">Representa a instância do **Win32 \_ TerminalService** que pode ser configurada com a propriedade **Setting** .</span><span class="sxs-lookup"><span data-stu-id="8fa83-129">Represents the instance of **Win32\_TerminalService** that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="8fa83-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8fa83-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fa83-131">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8fa83-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8fa83-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-133">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="8fa83-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8fa83-134">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8fa83-134">The date the object was installed.</span></span> <span data-ttu-id="8fa83-135">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="8fa83-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8fa83-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fa83-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fa83-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8fa83-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fa83-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8fa83-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8fa83-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fa83-140">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="8fa83-140">The name of the object.</span></span>

<span data-ttu-id="8fa83-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fa83-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fa83-142">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="8fa83-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fa83-143">Tipo de dados: **Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="8fa83-143">Data type: **Win32\_TSSessionDirectory**</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8fa83-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-145">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fa83-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fa83-146">Representa as configurações do agente de conexão de área de trabalho remota que podem ser aplicadas ao servidor Host da Sessão RD associado.</span><span class="sxs-lookup"><span data-stu-id="8fa83-146">Represents the RD Connection Broker settings that can be applied to the associated RD Session Host Server.</span></span>

</dd> <dt>

<span data-ttu-id="8fa83-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="8fa83-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fa83-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8fa83-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8fa83-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fa83-150">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8fa83-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8fa83-151">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8fa83-151">Current status of the object.</span></span> <span data-ttu-id="8fa83-152">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="8fa83-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8fa83-153">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="8fa83-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8fa83-154">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="8fa83-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8fa83-155">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="8fa83-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8fa83-156">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="8fa83-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8fa83-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fa83-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8fa83-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="8fa83-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fa83-159">("Erro")</span><span class="sxs-lookup"><span data-stu-id="8fa83-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fa83-160">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="8fa83-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fa83-161">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="8fa83-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fa83-162">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8fa83-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fa83-163">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="8fa83-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fa83-164">("Parando")</span><span class="sxs-lookup"><span data-stu-id="8fa83-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fa83-165">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="8fa83-165">("Service")</span></span>


<span data-ttu-id="8fa83-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8fa83-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8fa83-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fa83-167">Remarks</span></span>

<span data-ttu-id="8fa83-168">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8fa83-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8fa83-169">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8fa83-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8fa83-170">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="8fa83-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8fa83-171">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8fa83-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fa83-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fa83-172">Requirements</span></span>



| <span data-ttu-id="8fa83-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fa83-173">Requirement</span></span> | <span data-ttu-id="8fa83-174">Valor</span><span class="sxs-lookup"><span data-stu-id="8fa83-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fa83-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fa83-175">Minimum supported client</span></span><br/> | <span data-ttu-id="8fa83-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fa83-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fa83-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fa83-177">Minimum supported server</span></span><br/> | <span data-ttu-id="8fa83-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fa83-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fa83-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="8fa83-179">Namespace</span></span><br/>                | <span data-ttu-id="8fa83-180">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8fa83-180">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="8fa83-181">MOF</span><span class="sxs-lookup"><span data-stu-id="8fa83-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fa83-182"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fa83-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fa83-183">DLL</span><span class="sxs-lookup"><span data-stu-id="8fa83-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fa83-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fa83-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fa83-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fa83-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fa83-186">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="8fa83-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="8fa83-187">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="8fa83-187">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="8fa83-188">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="8fa83-188">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

