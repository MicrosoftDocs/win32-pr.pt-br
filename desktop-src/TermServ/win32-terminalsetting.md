---
title: Classe Win32_TerminalSetting
description: Representa as configurações que podem ser aplicadas a um terminal.
ms.assetid: e709aa60-f8fd-4e83-a5a1-d682ff469d23
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TerminalSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TerminalSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TerminalSetting
- Win32_TerminalSetting.Caption
- Win32_TerminalSetting.Description
- Win32_TerminalSetting.InstallDate
- Win32_TerminalSetting.Name
- Win32_TerminalSetting.Status
- Win32_TerminalSetting.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa29438ddea518c9f17e35fdafc3b9a912694d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757925"
---
# <a name="win32_terminalsetting-class"></a><span data-ttu-id="99749-105">\_Classe Win32 TerminalSetting</span><span class="sxs-lookup"><span data-stu-id="99749-105">Win32\_TerminalSetting class</span></span>

<span data-ttu-id="99749-106">A classe WMI **\_ TerminalSetting do Win32** representa as configurações que podem ser aplicadas a um terminal.</span><span class="sxs-lookup"><span data-stu-id="99749-106">The **Win32\_TerminalSetting** WMI class represents the settings that can be applied to a terminal.</span></span>

<span data-ttu-id="99749-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="99749-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="99749-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99749-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TerminalSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="99749-109">Membros</span><span class="sxs-lookup"><span data-stu-id="99749-109">Members</span></span>

<span data-ttu-id="99749-110">A classe **Win32 \_ TerminalSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="99749-110">The **Win32\_TerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="99749-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="99749-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99749-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="99749-112">Properties</span></span>

<span data-ttu-id="99749-113">A classe **Win32 \_ TerminalSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="99749-113">The **Win32\_TerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99749-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="99749-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99749-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="99749-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99749-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="99749-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99749-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="99749-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="99749-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="99749-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="99749-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="99749-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="99749-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="99749-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99749-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="99749-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99749-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="99749-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99749-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="99749-123">Description of the object.</span></span>

<span data-ttu-id="99749-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="99749-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="99749-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="99749-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99749-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="99749-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="99749-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="99749-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99749-128">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="99749-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="99749-129">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="99749-129">The date the object was installed.</span></span> <span data-ttu-id="99749-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="99749-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="99749-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="99749-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="99749-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="99749-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99749-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="99749-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99749-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="99749-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99749-135">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="99749-135">The name of the object.</span></span>

<span data-ttu-id="99749-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="99749-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="99749-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="99749-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99749-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="99749-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99749-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="99749-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99749-140">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="99749-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="99749-141">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="99749-141">Current status of the object.</span></span> <span data-ttu-id="99749-142">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="99749-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="99749-143">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="99749-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="99749-144">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="99749-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="99749-145">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="99749-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="99749-146">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="99749-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="99749-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="99749-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="99749-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="99749-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="99749-149">("Erro")</span><span class="sxs-lookup"><span data-stu-id="99749-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="99749-150">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="99749-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="99749-151">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="99749-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="99749-152">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="99749-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="99749-153">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="99749-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="99749-154">("Parando")</span><span class="sxs-lookup"><span data-stu-id="99749-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="99749-155">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="99749-155">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="99749-156">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="99749-156">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99749-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="99749-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99749-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="99749-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99749-159">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="99749-159">The name of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99749-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="99749-160">Remarks</span></span>

<span data-ttu-id="99749-161">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="99749-161">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="99749-162">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="99749-162">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="99749-163">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="99749-163">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="99749-164">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="99749-164">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="99749-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99749-165">Requirements</span></span>



| <span data-ttu-id="99749-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="99749-166">Requirement</span></span> | <span data-ttu-id="99749-167">Valor</span><span class="sxs-lookup"><span data-stu-id="99749-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99749-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99749-168">Minimum supported client</span></span><br/> | <span data-ttu-id="99749-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99749-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99749-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99749-170">Minimum supported server</span></span><br/> | <span data-ttu-id="99749-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99749-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99749-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="99749-172">Namespace</span></span><br/>                | <span data-ttu-id="99749-173">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="99749-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="99749-174">MOF</span><span class="sxs-lookup"><span data-stu-id="99749-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99749-175"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99749-175"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="99749-176">DLL</span><span class="sxs-lookup"><span data-stu-id="99749-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99749-177"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99749-177"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99749-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="99749-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99749-179">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="99749-179">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="99749-180">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="99749-180">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="99749-181">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="99749-181">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

