---
title: Classe CIM_ElementSetting (Serviços de Área de Trabalho Remota)
description: Representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.
ms.assetid: b74c2fef-0f3a-46b9-9dd8-11016a8f7b57
ms.tgt_platform: multiple
keywords:
- Classe de CIM_ElementSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de CIM_ElementSetting classe, descrita
topic_type:
- apiref
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Caption
- CIM_ElementSetting.Description
- CIM_ElementSetting.InstallDate
- CIM_ElementSetting.Name
- CIM_ElementSetting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aff40961ddc8fa07de6c49d6c95aefe3d005d6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085275"
---
# <a name="cim_elementsetting-class-remote-desktop-services"></a><span data-ttu-id="746e5-105">Classe CIM_ElementSetting (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="746e5-105">CIM_ElementSetting class (Remote Desktop Services)</span></span>

<span data-ttu-id="746e5-106">Representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.</span><span class="sxs-lookup"><span data-stu-id="746e5-106">Represents the association between managed system elements and the setting class defined for them.</span></span>

<span data-ttu-id="746e5-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="746e5-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="746e5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="746e5-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="746e5-109">Membros</span><span class="sxs-lookup"><span data-stu-id="746e5-109">Members</span></span>

<span data-ttu-id="746e5-110">A classe **CIM \_ ElementSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="746e5-110">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="746e5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="746e5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="746e5-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="746e5-112">Properties</span></span>

<span data-ttu-id="746e5-113">A classe **CIM \_ ElementSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="746e5-113">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="746e5-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="746e5-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="746e5-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="746e5-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="746e5-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="746e5-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="746e5-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="746e5-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="746e5-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="746e5-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="746e5-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="746e5-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="746e5-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="746e5-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="746e5-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="746e5-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="746e5-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="746e5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="746e5-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="746e5-123">Description of the object.</span></span>

<span data-ttu-id="746e5-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="746e5-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="746e5-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="746e5-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="746e5-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="746e5-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="746e5-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="746e5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="746e5-128">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="746e5-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="746e5-129">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="746e5-129">The date the object was installed.</span></span> <span data-ttu-id="746e5-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="746e5-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="746e5-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="746e5-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="746e5-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="746e5-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="746e5-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="746e5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="746e5-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="746e5-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="746e5-135">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="746e5-135">The name of the object.</span></span>

<span data-ttu-id="746e5-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="746e5-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="746e5-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="746e5-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="746e5-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="746e5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="746e5-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="746e5-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="746e5-140">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="746e5-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="746e5-141">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="746e5-141">Current status of the object.</span></span> <span data-ttu-id="746e5-142">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="746e5-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="746e5-143">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="746e5-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="746e5-144">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="746e5-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="746e5-145">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="746e5-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="746e5-146">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="746e5-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="746e5-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="746e5-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="746e5-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="746e5-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="746e5-149">("Erro")</span><span class="sxs-lookup"><span data-stu-id="746e5-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="746e5-150">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="746e5-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="746e5-151">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="746e5-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="746e5-152">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="746e5-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="746e5-153">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="746e5-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="746e5-154">("Parando")</span><span class="sxs-lookup"><span data-stu-id="746e5-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="746e5-155">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="746e5-155">("Service")</span></span>


<span data-ttu-id="746e5-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="746e5-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="746e5-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="746e5-157">Requirements</span></span>



| <span data-ttu-id="746e5-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="746e5-158">Requirement</span></span> | <span data-ttu-id="746e5-159">Valor</span><span class="sxs-lookup"><span data-stu-id="746e5-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="746e5-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="746e5-160">Minimum supported client</span></span><br/> | <span data-ttu-id="746e5-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="746e5-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="746e5-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="746e5-162">Minimum supported server</span></span><br/> | <span data-ttu-id="746e5-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="746e5-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="746e5-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="746e5-164">Namespace</span></span><br/>                | <span data-ttu-id="746e5-165">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="746e5-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="746e5-166">MOF</span><span class="sxs-lookup"><span data-stu-id="746e5-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="746e5-167"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="746e5-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="746e5-168">DLL</span><span class="sxs-lookup"><span data-stu-id="746e5-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="746e5-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="746e5-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="746e5-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="746e5-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="746e5-171">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="746e5-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

