---
title: Classe CIM_Setting (Serviços de Área de Trabalho Remota)
description: Representa parâmetros operacionais e relacionados à configuração para um ou mais elementos do sistema gerenciado.
ms.assetid: d0007762-5d13-421b-a73a-3392a77686a6
ms.tgt_platform: multiple
keywords:
- Classe de CIM_Setting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de CIM_Setting classe, descrita
topic_type:
- apiref
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.InstallDate
- CIM_Setting.Name
- CIM_Setting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d3a9517df9af92f428000ed064b2bb88b348a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759033"
---
# <a name="cim_setting-class-remote-desktop-services"></a><span data-ttu-id="89f69-105">Classe CIM_Setting (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="89f69-105">CIM_Setting class (Remote Desktop Services)</span></span>

<span data-ttu-id="89f69-106">Representa parâmetros operacionais e relacionados à configuração para um ou mais elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="89f69-106">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

<span data-ttu-id="89f69-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="89f69-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f69-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89f69-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="89f69-109">Membros</span><span class="sxs-lookup"><span data-stu-id="89f69-109">Members</span></span>

<span data-ttu-id="89f69-110">A classe de **\_ configuração CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="89f69-110">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="89f69-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89f69-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89f69-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89f69-112">Properties</span></span>

<span data-ttu-id="89f69-113">A classe de **\_ configuração CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="89f69-113">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89f69-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="89f69-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f69-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89f69-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f69-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89f69-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f69-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="89f69-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="89f69-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="89f69-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="89f69-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89f69-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f69-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="89f69-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f69-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89f69-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f69-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89f69-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89f69-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="89f69-123">Description of the object.</span></span>

<span data-ttu-id="89f69-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89f69-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f69-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="89f69-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f69-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="89f69-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="89f69-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89f69-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f69-128">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="89f69-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="89f69-129">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="89f69-129">The date the object was installed.</span></span> <span data-ttu-id="89f69-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="89f69-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="89f69-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89f69-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f69-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="89f69-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f69-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89f69-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f69-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89f69-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89f69-135">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="89f69-135">The name of the object.</span></span>

<span data-ttu-id="89f69-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89f69-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f69-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="89f69-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f69-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89f69-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f69-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89f69-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f69-140">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="89f69-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="89f69-141">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="89f69-141">Current status of the object.</span></span> <span data-ttu-id="89f69-142">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="89f69-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="89f69-143">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="89f69-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="89f69-144">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="89f69-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="89f69-145">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="89f69-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="89f69-146">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="89f69-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="89f69-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="89f69-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="89f69-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="89f69-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89f69-149">("Erro")</span><span class="sxs-lookup"><span data-stu-id="89f69-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89f69-150">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="89f69-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89f69-151">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="89f69-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89f69-152">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="89f69-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89f69-153">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="89f69-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89f69-154">("Parando")</span><span class="sxs-lookup"><span data-stu-id="89f69-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="89f69-155">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="89f69-155">("Service")</span></span>


<span data-ttu-id="89f69-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="89f69-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="89f69-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89f69-157">Requirements</span></span>



| <span data-ttu-id="89f69-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="89f69-158">Requirement</span></span> | <span data-ttu-id="89f69-159">Valor</span><span class="sxs-lookup"><span data-stu-id="89f69-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89f69-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89f69-160">Minimum supported client</span></span><br/> | <span data-ttu-id="89f69-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89f69-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89f69-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89f69-162">Minimum supported server</span></span><br/> | <span data-ttu-id="89f69-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89f69-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89f69-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="89f69-164">Namespace</span></span><br/>                | <span data-ttu-id="89f69-165">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="89f69-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="89f69-166">MOF</span><span class="sxs-lookup"><span data-stu-id="89f69-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89f69-167"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89f69-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="89f69-168">DLL</span><span class="sxs-lookup"><span data-stu-id="89f69-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89f69-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89f69-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89f69-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="89f69-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f69-171">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="89f69-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

