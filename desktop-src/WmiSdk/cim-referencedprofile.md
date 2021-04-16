---
description: Usado para associar uma \_ RegisteredProfile de CIM de instância a uma instância de CIM \_ RegisteredProfile de outro perfil que faz referência ao perfil dependente como um perfil relacionado.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: Classe CIM_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751139"
---
# <a name="cim_referencedprofile-class"></a><span data-ttu-id="8c79c-103">\_Classe CIM ReferencedProfile</span><span class="sxs-lookup"><span data-stu-id="8c79c-103">CIM\_ReferencedProfile class</span></span>

<span data-ttu-id="8c79c-104">Usado para associar uma [**\_ RegisteredProfile de CIM**](/previous-versions//ee309375(v=vs.85)) de instância a uma instância de **CIM \_ RegisteredProfile** de outro perfil que faz referência ao perfil dependente como um perfil relacionado.</span><span class="sxs-lookup"><span data-stu-id="8c79c-104">Used to associate an instance [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) with an instance of **CIM\_RegisteredProfile** of another profile that references the dependent profile as a related profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c79c-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8c79c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8c79c-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8c79c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8c79c-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8c79c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c79c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c79c-108">Syntax</span></span>

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8c79c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8c79c-109">Members</span></span>

<span data-ttu-id="8c79c-110">A classe **CIM \_ ReferencedProfile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8c79c-110">The **CIM\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="8c79c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8c79c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c79c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8c79c-112">Properties</span></span>

<span data-ttu-id="8c79c-113">A classe **CIM \_ ReferencedProfile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8c79c-113">The **CIM\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c79c-114">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="8c79c-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c79c-115">Tipo de dados: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="8c79c-115">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="8c79c-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8c79c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c79c-117">Especifica a instância de [**\_ RegisteredProfile do CIM**](/previous-versions//ee309375(v=vs.85)) que é referenciada pelo perfil **dependente** .</span><span class="sxs-lookup"><span data-stu-id="8c79c-117">Specifies the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="8c79c-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="8c79c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c79c-119">Tipo de dados: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="8c79c-119">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="8c79c-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8c79c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c79c-121">Especifica uma instância de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)) que faz referência a outros perfis.</span><span class="sxs-lookup"><span data-stu-id="8c79c-121">Specifies a [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that references other profiles.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c79c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c79c-122">Remarks</span></span>

<span data-ttu-id="8c79c-123">O uso das propriedades **dependent** e **Antecedent** na associação **\_ ReferencedProfile do CIM** é definido de modo que o perfil que está sendo referenciado seja o antecedente e o perfil que faz a referência seja o dependente.</span><span class="sxs-lookup"><span data-stu-id="8c79c-123">The use of the **Dependent** and **Antecedent** properties in the **CIM\_ReferencedProfile** association is defined such that the profile being referenced is the antecedent and the profile doing the referencing is the dependent.</span></span>

<span data-ttu-id="8c79c-124">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8c79c-124">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8c79c-125">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8c79c-125">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c79c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c79c-126">Requirements</span></span>



| <span data-ttu-id="8c79c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c79c-127">Requirement</span></span> | <span data-ttu-id="8c79c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8c79c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c79c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c79c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8c79c-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c79c-130">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="8c79c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c79c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8c79c-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8c79c-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="8c79c-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c79c-133">Namespace</span></span><br/>                | <span data-ttu-id="8c79c-134">\\Interoperabilidade raiz</span><span class="sxs-lookup"><span data-stu-id="8c79c-134">Root\\interop</span></span><br/>                                                               |
| <span data-ttu-id="8c79c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8c79c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c79c-136"><dt>Interop. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c79c-136"><dt>Interop.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c79c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c79c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c79c-138">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="8c79c-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

