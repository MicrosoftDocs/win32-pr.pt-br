---
title: Classe CIM_ManagedSystemElement (Serviços de Área de Trabalho Remota)
description: A classe base para a hierarquia de elementos do sistema.
ms.assetid: c71c0441-381f-4a46-864c-9206c43a27d0
ms.tgt_platform: multiple
keywords:
- Classe de CIM_ManagedSystemElement Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de CIM_ManagedSystemElement classe, descrita
topic_type:
- apiref
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b242369df24724fdcc31ce925a229dba5bb515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085274"
---
# <a name="cim_managedsystemelement-class-remote-desktop-services"></a><span data-ttu-id="ffc19-105">Classe CIM_ManagedSystemElement (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="ffc19-105">CIM_ManagedSystemElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="ffc19-106">A classe base para a hierarquia de elementos do sistema.</span><span class="sxs-lookup"><span data-stu-id="ffc19-106">The base class for the system element hierarchy.</span></span>

<span data-ttu-id="ffc19-107">Qualquer componente de sistema diferencial é um candidato para inclusão nessa classe.</span><span class="sxs-lookup"><span data-stu-id="ffc19-107">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="ffc19-108">Os exemplos incluem componentes de software, como arquivos; dispositivos, como unidades de disco e controladores; e componentes físicos, como chips e cartões</span><span class="sxs-lookup"><span data-stu-id="ffc19-108">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards</span></span>

<span data-ttu-id="ffc19-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ffc19-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc19-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffc19-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="ffc19-111">Membros</span><span class="sxs-lookup"><span data-stu-id="ffc19-111">Members</span></span>

<span data-ttu-id="ffc19-112">A classe **CIM \_ ManagedSystemElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ffc19-112">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ffc19-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ffc19-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffc19-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ffc19-114">Properties</span></span>

<span data-ttu-id="ffc19-115">A classe **CIM \_ ManagedSystemElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ffc19-115">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffc19-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ffc19-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc19-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ffc19-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc19-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ffc19-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffc19-119">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ffc19-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ffc19-120">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc19-120">Short description (one-line string) of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ffc19-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ffc19-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc19-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ffc19-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc19-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ffc19-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffc19-124">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc19-124">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ffc19-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ffc19-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc19-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ffc19-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ffc19-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ffc19-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffc19-128">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="ffc19-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ffc19-129">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="ffc19-129">The date the object was installed.</span></span> <span data-ttu-id="ffc19-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="ffc19-130">A lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="ffc19-131">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ffc19-131">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc19-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ffc19-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc19-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ffc19-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffc19-134">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc19-134">The name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ffc19-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="ffc19-135">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc19-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ffc19-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc19-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ffc19-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffc19-138">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ffc19-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ffc19-139">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc19-139">Current status of the object.</span></span> <span data-ttu-id="ffc19-140">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="ffc19-140">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ffc19-141">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="ffc19-141">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ffc19-142">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="ffc19-142">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ffc19-143">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="ffc19-143">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ffc19-144">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="ffc19-144">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<dt>



 <span data-ttu-id="ffc19-145">("OK")</span><span class="sxs-lookup"><span data-stu-id="ffc19-145">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ffc19-146">("Erro")</span><span class="sxs-lookup"><span data-stu-id="ffc19-146">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ffc19-147">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="ffc19-147">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ffc19-148">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="ffc19-148">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ffc19-149">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ffc19-149">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ffc19-150">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="ffc19-150">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ffc19-151">("Parando")</span><span class="sxs-lookup"><span data-stu-id="ffc19-151">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ffc19-152">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="ffc19-152">("Service")</span></span>


<span data-ttu-id="ffc19-153"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ffc19-153"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ffc19-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffc19-154">Requirements</span></span>



| <span data-ttu-id="ffc19-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffc19-155">Requirement</span></span> | <span data-ttu-id="ffc19-156">Valor</span><span class="sxs-lookup"><span data-stu-id="ffc19-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc19-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffc19-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ffc19-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffc19-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ffc19-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffc19-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ffc19-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffc19-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ffc19-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffc19-161">Namespace</span></span><br/>                | <span data-ttu-id="ffc19-162">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="ffc19-162">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ffc19-163">MOF</span><span class="sxs-lookup"><span data-stu-id="ffc19-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffc19-164"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffc19-164"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffc19-165">DLL</span><span class="sxs-lookup"><span data-stu-id="ffc19-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffc19-166"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffc19-166"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

