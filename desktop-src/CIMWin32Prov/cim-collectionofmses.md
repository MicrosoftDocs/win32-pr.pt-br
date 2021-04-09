---
description: O \_ objeto CIM CollectionOfMSEs permite o agrupamento de \_ objetos CIM ManagedSystemElement com a finalidade de associar definições e configurações. É abstrato exigir mais definição e refinamento semântico em subclasses.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: Classe CIM_CollectionOfMSEs (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089351"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="3e1dd-104">Classe CIM_CollectionOfMSEs (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3e1dd-104">CIM_CollectionOfMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3e1dd-105">O objeto **CIM \_ CollectionOfMSEs** permite o agrupamento de objetos [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) com a finalidade de associar definições e configurações.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-105">The **CIM\_CollectionOfMSEs** object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="3e1dd-106">É abstrato exigir mais definição e refinamento semântico em subclasses.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-106">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

<span data-ttu-id="3e1dd-107">O objeto **CIM \_ CollectionOfMSEs** não carrega nenhuma informação de estado ou status, mas representa apenas um agrupamento de elementos.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-107">The **CIM\_CollectionOfMSEs** object does not carry any state or status information, but only represents a grouping of elements.</span></span> <span data-ttu-id="3e1dd-108">Por esse motivo, ele está incorreto para grupos de subclasses que têm estado/status do **CIM \_ CollectionOfMSEs**, um exemplo é o [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (que é subclasse corretamente de [**CIM \_ LogicalElement**](cim-logicalelement.md)).</span><span class="sxs-lookup"><span data-stu-id="3e1dd-108">For this reason, it is incorrect to subclass groups that have state/status from **CIM\_CollectionOfMSEs**, An example is [**CIM\_RedundancyGroup**](cim-redundancygroup.md) (which is correctly subclassed from [**CIM\_LogicalElement**](cim-logicalelement.md)).</span></span> <span data-ttu-id="3e1dd-109">Normalmente, as coleções agregam objetos ' like ' e representam uma otimização.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-109">Collections typically aggregate 'like' objects, and represent an optimization.</span></span> <span data-ttu-id="3e1dd-110">Sem coleções, uma é forçada a definir as associações [**\_ ElementSetting**](cim-elementsetting.md) e CIM [**\_ ElementConfiguration**](cim-elementconfiguration.md) individuais para vincular configurações e objetos de configuração a [**\_ ManagedSystemElements CIM**](cim-managedsystemelement.md)individuais.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-110">Without collections, one is forced to define individual [**CIM\_ElementSetting**](cim-elementsetting.md) and [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) associations, to tie settings and configuration objects to individual [**CIM\_ManagedSystemElements**](cim-managedsystemelement.md).</span></span> <span data-ttu-id="3e1dd-111">Pode haver muita duplicação ao atribuir a mesma configuração a vários objetos.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-111">There may be much duplication in assigning the same setting to multiple objects.</span></span> <span data-ttu-id="3e1dd-112">Além disso, o uso do objeto de coleção permite determinar se as associações de configuração e configuração são realmente as mesmas para os membros da coleção.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-112">In addition, using the collection object allows the determination that the setting and configuration associations are indeed the same for the collection's members.</span></span> <span data-ttu-id="3e1dd-113">Por outro lado, essas informações seriam obtidas definindo a coleção de forma proprietária e, em seguida, consultando as associações **CIM \_ ElementSetting** e **CIM \_ ElementConfiguration** para determinar se o conjunto de coleta foi totalmente coberto.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-113">This information would otherwise be obtained by defining the collection in a proprietary manner, and then querying the **CIM\_ElementSetting** and **CIM\_ElementConfiguration** associations to determine if the collection set is completely covered.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e1dd-114">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3e1dd-115">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3e1dd-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3e1dd-116">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3e1dd-117">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e1dd-118">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e1dd-118">Syntax</span></span>

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a><span data-ttu-id="3e1dd-119">Membros</span><span class="sxs-lookup"><span data-stu-id="3e1dd-119">Members</span></span>

<span data-ttu-id="3e1dd-120">A classe **CIM \_ CollectionOfMSEs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3e1dd-120">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="3e1dd-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e1dd-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e1dd-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e1dd-122">Properties</span></span>

<span data-ttu-id="3e1dd-123">A classe **CIM \_ CollectionOfMSEs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-123">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e1dd-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="3e1dd-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1dd-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e1dd-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1dd-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e1dd-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1dd-127">Breve descrição textual do objeto CollectionOfMSEs.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-127">Short textual description of the CollectionOfMSEs object.</span></span>

</dd> <dt>

<span data-ttu-id="3e1dd-128">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="3e1dd-128">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1dd-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e1dd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1dd-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e1dd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1dd-131">Identificação do objeto de coleção.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-131">Identification of the Collection object.</span></span> <span data-ttu-id="3e1dd-132">Quando em uma subclasse, a propriedade CollectionId pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-132">When subclassed, the CollectionID property can be overridden to be a Key property.</span></span>

</dd> <dt>

<span data-ttu-id="3e1dd-133">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3e1dd-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e1dd-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e1dd-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e1dd-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e1dd-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e1dd-136">Descrição textual do objeto CollectionOfMSEs.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-136">Textual description of the CollectionOfMSEs object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e1dd-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e1dd-137">Remarks</span></span>

<span data-ttu-id="3e1dd-138">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-138">WMI does not implement this class.</span></span> <span data-ttu-id="3e1dd-139">Consulte [classes Win32](win32-provider.md) para classes WMI derivadas do **CIM \_ CollectionOfMSEs**.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-139">See [Win32 Classes](win32-provider.md) for WMI classes derived from **CIM\_CollectionOfMSEs**.</span></span>

<span data-ttu-id="3e1dd-140">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-140">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3e1dd-141">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3e1dd-141">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e1dd-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e1dd-142">Requirements</span></span>



| <span data-ttu-id="3e1dd-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e1dd-143">Requirement</span></span> | <span data-ttu-id="3e1dd-144">Valor</span><span class="sxs-lookup"><span data-stu-id="3e1dd-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e1dd-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e1dd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3e1dd-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e1dd-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e1dd-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e1dd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3e1dd-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e1dd-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e1dd-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e1dd-149">Namespace</span></span><br/>                | <span data-ttu-id="3e1dd-150">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3e1dd-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e1dd-151">MOF</span><span class="sxs-lookup"><span data-stu-id="3e1dd-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e1dd-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e1dd-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e1dd-153">DLL</span><span class="sxs-lookup"><span data-stu-id="3e1dd-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e1dd-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e1dd-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




