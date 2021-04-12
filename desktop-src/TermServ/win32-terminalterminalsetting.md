---
title: Classe Win32_TerminalTerminalSetting
description: Representa a associação entre um terminal e seus parâmetros de configuração.
ms.assetid: c92d79ec-eca5-4a73-a89a-dfc55474d88b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TerminalTerminalSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TerminalTerminalSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TerminalTerminalSetting
- Win32_TerminalTerminalSetting.Caption
- Win32_TerminalTerminalSetting.Description
- Win32_TerminalTerminalSetting.InstallDate
- Win32_TerminalTerminalSetting.Name
- Win32_TerminalTerminalSetting.Status
- Win32_TerminalTerminalSetting.Element
- Win32_TerminalTerminalSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9e3b251ef81a6fab43d4973a8148c78f312ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455040"
---
# <a name="win32_terminalterminalsetting-class"></a><span data-ttu-id="6f4d8-105">\_Classe Win32 TerminalTerminalSetting</span><span class="sxs-lookup"><span data-stu-id="6f4d8-105">Win32\_TerminalTerminalSetting class</span></span>

<span data-ttu-id="6f4d8-106">A classe WMI **\_ TerminalTerminalSetting do Win32** representa a associação entre um terminal e suas definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-106">The **Win32\_TerminalTerminalSetting** WMI class represents the association between a terminal and its configuration settings.</span></span>

<span data-ttu-id="6f4d8-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-107">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4d8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f4d8-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALTERMINALSETTING_Prov"), AMENDMENT]
class Win32_TerminalTerminalSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_Terminal        REF Element;
  Win32_TerminalSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="6f4d8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6f4d8-109">Members</span></span>

<span data-ttu-id="6f4d8-110">A classe **Win32 \_ TerminalTerminalSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6f4d8-110">The **Win32\_TerminalTerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="6f4d8-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f4d8-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f4d8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f4d8-112">Properties</span></span>

<span data-ttu-id="6f4d8-113">A classe **Win32 \_ TerminalTerminalSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-113">The **Win32\_TerminalTerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f4d8-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4d8-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f4d8-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6f4d8-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6f4d8-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6f4d8-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f4d8-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f4d8-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4d8-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f4d8-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f4d8-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-123">Description of the object.</span></span>

<span data-ttu-id="6f4d8-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f4d8-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f4d8-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4d8-126">Tipo de dados **: \_ terminal do Win32**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-126">Data type: **Win32\_Terminal**</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f4d8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f4d8-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6f4d8-129">Representa o terminal que pode ser configurado por meio da propriedade **Setting** .</span><span class="sxs-lookup"><span data-stu-id="6f4d8-129">Represents the terminal that can be configured through the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="6f4d8-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4d8-131">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f4d8-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-133">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="6f4d8-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6f4d8-134">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-134">The date the object was installed.</span></span> <span data-ttu-id="6f4d8-135">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6f4d8-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f4d8-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f4d8-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4d8-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f4d8-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f4d8-140">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-140">The name of the object.</span></span>

<span data-ttu-id="6f4d8-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f4d8-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f4d8-142">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4d8-143">Tipo de dados: **Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-143">Data type: **Win32\_TerminalSetting**</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f4d8-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-145">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f4d8-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6f4d8-146">Representa as configurações que podem ser aplicadas ao terminal especificado.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-146">Represents the settings that can be applied to the specified terminal.</span></span>

</dd> <dt>

<span data-ttu-id="6f4d8-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4d8-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f4d8-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f4d8-150">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="6f4d8-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6f4d8-151">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-151">Current status of the object.</span></span> <span data-ttu-id="6f4d8-152">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6f4d8-153">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="6f4d8-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6f4d8-154">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="6f4d8-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6f4d8-155">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6f4d8-156">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6f4d8-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f4d8-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6f4d8-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="6f4d8-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f4d8-159">("Erro")</span><span class="sxs-lookup"><span data-stu-id="6f4d8-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f4d8-160">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="6f4d8-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f4d8-161">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6f4d8-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f4d8-162">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6f4d8-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f4d8-163">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6f4d8-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f4d8-164">("Parando")</span><span class="sxs-lookup"><span data-stu-id="6f4d8-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f4d8-165">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="6f4d8-165">("Service")</span></span>


<span data-ttu-id="6f4d8-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6f4d8-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6f4d8-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f4d8-167">Remarks</span></span>

<span data-ttu-id="6f4d8-168">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6f4d8-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6f4d8-169">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6f4d8-170">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6f4d8-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6f4d8-171">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6f4d8-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f4d8-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f4d8-172">Requirements</span></span>



| <span data-ttu-id="6f4d8-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f4d8-173">Requirement</span></span> | <span data-ttu-id="6f4d8-174">Valor</span><span class="sxs-lookup"><span data-stu-id="6f4d8-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4d8-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f4d8-175">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4d8-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f4d8-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f4d8-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f4d8-177">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4d8-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f4d8-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f4d8-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f4d8-179">Namespace</span></span><br/>                | <span data-ttu-id="6f4d8-180">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6f4d8-180">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6f4d8-181">MOF</span><span class="sxs-lookup"><span data-stu-id="6f4d8-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f4d8-182"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f4d8-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f4d8-183">DLL</span><span class="sxs-lookup"><span data-stu-id="6f4d8-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f4d8-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f4d8-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f4d8-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f4d8-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4d8-186">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="6f4d8-187">**Terminal do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-187">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="6f4d8-188">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="6f4d8-188">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

