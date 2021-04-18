---
title: Classe Win32_TSVirtualIPSetting
description: Representa a associação entre uma \_ classe de elemento TerminalService do Win32 e uma \_ classe de configuração Win32 TSVirtualIP.
ms.assetid: 06a78b4d-973a-4912-b7e6-bc490197c4a6
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSVirtualIPSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSVirtualIPSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSVirtualIPSetting
- Win32_TSVirtualIPSetting.Caption
- Win32_TSVirtualIPSetting.Description
- Win32_TSVirtualIPSetting.InstallDate
- Win32_TSVirtualIPSetting.Name
- Win32_TSVirtualIPSetting.Status
- Win32_TSVirtualIPSetting.Element
- Win32_TSVirtualIPSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7368b3b2e932f45d047d4ca4db724030b2dd82ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105767718"
---
# <a name="win32_tsvirtualipsetting-class"></a><span data-ttu-id="46aee-105">\_Classe Win32 TSVirtualIPSetting</span><span class="sxs-lookup"><span data-stu-id="46aee-105">Win32\_TSVirtualIPSetting class</span></span>

<span data-ttu-id="46aee-106">Representa a associação entre uma classe de elemento [**\_ TerminalService do Win32**](win32-terminalservice.md) e uma classe de configuração [**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="46aee-106">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

<span data-ttu-id="46aee-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="46aee-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46aee-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46aee-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSVIRTUALIPSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIPSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_TerminalService REF Element;
  Win32_TSVirtualIP     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="46aee-109">Membros</span><span class="sxs-lookup"><span data-stu-id="46aee-109">Members</span></span>

<span data-ttu-id="46aee-110">A classe **Win32 \_ TSVirtualIPSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="46aee-110">The **Win32\_TSVirtualIPSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="46aee-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46aee-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46aee-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46aee-112">Properties</span></span>

<span data-ttu-id="46aee-113">A classe **Win32 \_ TSVirtualIPSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="46aee-113">The **Win32\_TSVirtualIPSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46aee-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="46aee-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46aee-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46aee-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46aee-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46aee-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46aee-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="46aee-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="46aee-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="46aee-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="46aee-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46aee-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46aee-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46aee-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46aee-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46aee-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46aee-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46aee-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46aee-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="46aee-123">Description of the object.</span></span>

<span data-ttu-id="46aee-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46aee-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46aee-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="46aee-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46aee-126">Tipo de dados: **[ **Win32 \_ TerminalService**](win32-terminalservice.md)**</span><span class="sxs-lookup"><span data-stu-id="46aee-126">Data type: **[**Win32\_TerminalService**](win32-terminalservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="46aee-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46aee-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46aee-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46aee-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46aee-129">Uma referência a um [**objeto \_ TerminalService do Win32**](win32-terminalservice.md) que é a classe do elemento para a associação.</span><span class="sxs-lookup"><span data-stu-id="46aee-129">A reference to a [**Win32\_TerminalService**](win32-terminalservice.md) object that is the element class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="46aee-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="46aee-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46aee-131">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="46aee-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="46aee-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46aee-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46aee-133">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="46aee-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="46aee-134">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="46aee-134">The date the object was installed.</span></span> <span data-ttu-id="46aee-135">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="46aee-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="46aee-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46aee-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46aee-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="46aee-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46aee-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46aee-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46aee-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46aee-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46aee-140">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="46aee-140">The name of the object.</span></span>

<span data-ttu-id="46aee-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46aee-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46aee-142">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="46aee-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46aee-143">Tipo de dados: **[ **Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)**</span><span class="sxs-lookup"><span data-stu-id="46aee-143">Data type: **[**Win32\_TSVirtualIP**](win32-tsvirtualip.md)**</span></span>
</dt> <dt>

<span data-ttu-id="46aee-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46aee-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46aee-145">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46aee-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46aee-146">Uma referência a um [**objeto \_ TSVirtualIP do Win32**](win32-tsvirtualip.md) que é a classe de configuração para a associação.</span><span class="sxs-lookup"><span data-stu-id="46aee-146">A reference to a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) object that is the setting class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="46aee-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="46aee-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46aee-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46aee-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46aee-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46aee-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46aee-150">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="46aee-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="46aee-151">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="46aee-151">Current status of the object.</span></span> <span data-ttu-id="46aee-152">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="46aee-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="46aee-153">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="46aee-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="46aee-154">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="46aee-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="46aee-155">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="46aee-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="46aee-156">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="46aee-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="46aee-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46aee-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="46aee-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="46aee-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46aee-159">("Erro")</span><span class="sxs-lookup"><span data-stu-id="46aee-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46aee-160">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="46aee-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46aee-161">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="46aee-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46aee-162">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="46aee-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46aee-163">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="46aee-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46aee-164">("Parando")</span><span class="sxs-lookup"><span data-stu-id="46aee-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46aee-165">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="46aee-165">("Service")</span></span>


<span data-ttu-id="46aee-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="46aee-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="46aee-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46aee-167">Requirements</span></span>



| <span data-ttu-id="46aee-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="46aee-168">Requirement</span></span> | <span data-ttu-id="46aee-169">Valor</span><span class="sxs-lookup"><span data-stu-id="46aee-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46aee-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46aee-170">Minimum supported client</span></span><br/> | <span data-ttu-id="46aee-171">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="46aee-171">None supported</span></span><br/>                                                               |
| <span data-ttu-id="46aee-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46aee-172">Minimum supported server</span></span><br/> | <span data-ttu-id="46aee-173">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46aee-173">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="46aee-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="46aee-174">Namespace</span></span><br/>                | <span data-ttu-id="46aee-175">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="46aee-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="46aee-176">MOF</span><span class="sxs-lookup"><span data-stu-id="46aee-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46aee-177"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46aee-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="46aee-178">DLL</span><span class="sxs-lookup"><span data-stu-id="46aee-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46aee-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46aee-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46aee-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="46aee-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46aee-181">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="46aee-181">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="46aee-182">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="46aee-182">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="46aee-183">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="46aee-183">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

