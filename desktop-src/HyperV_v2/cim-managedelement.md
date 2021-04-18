---
description: A \_ classe CIM managedelement é uma classe abstrata que fornece uma superclasse comum (ou a parte superior da árvore de herança) para as classes de não associação no esquema CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: Classe CIM_ManagedElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761720"
---
# <a name="cim_managedelement-class"></a><span data-ttu-id="15321-103">\_Classe managedelement CIM</span><span class="sxs-lookup"><span data-stu-id="15321-103">CIM\_ManagedElement class</span></span>

<span data-ttu-id="15321-104">A classe **CIM \_ managedelement** é uma classe abstrata que fornece uma superclasse comum (ou a parte superior da árvore de herança) para as classes de não associação no esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="15321-104">The **CIM\_ManagedElement** class is an abstract class that provides a common superclass (or top of the inheritance tree) for the non-association classes in the CIM Schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="15321-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15321-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="15321-106">Membros</span><span class="sxs-lookup"><span data-stu-id="15321-106">Members</span></span>

<span data-ttu-id="15321-107">A classe **CIM \_ managedelement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="15321-107">The **CIM\_ManagedElement** class has these types of members:</span></span>

-   [<span data-ttu-id="15321-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="15321-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15321-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="15321-109">Properties</span></span>

<span data-ttu-id="15321-110">A classe **CIM \_ managedelement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="15321-110">The **CIM\_ManagedElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15321-111">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="15321-111">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15321-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15321-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15321-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15321-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15321-114">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="15321-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="15321-115">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="15321-115">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="15321-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="15321-116">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15321-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15321-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15321-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15321-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15321-119">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="15321-119">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="15321-120">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="15321-120">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15321-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15321-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15321-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15321-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15321-123">Um nome amigável para o objeto.</span><span class="sxs-lookup"><span data-stu-id="15321-123">A user-friendly name for the object.</span></span> <span data-ttu-id="15321-124">Essa propriedade permite que cada instância defina um nome amigável de usuário, além de suas propriedades de chave, dados de identidade e informações de descrição.</span><span class="sxs-lookup"><span data-stu-id="15321-124">This property allows each instance to define a user-friendly name in addition to its key properties, identity data, and description information.</span></span>

</dd> <dt>

<span data-ttu-id="15321-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="15321-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15321-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15321-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15321-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15321-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15321-128">Identifica exclusivamente e de forma opaca uma instância dessa classe dentro do escopo do namespace que a contém.</span><span class="sxs-lookup"><span data-stu-id="15321-128">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="15321-129">Para garantir a exclusividade no namespace, o valor da propriedade **InstanceId** deve ser construído no seguinte padrão: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="15321-129">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="15321-130">*OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que define a **InstanceId** ou ser uma ID registrada que é atribuída por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="15321-130">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="15321-131">Esse padrão é semelhante à estrutura de nomes de classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="15321-131">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="15321-132">Além disso, para garantir a exclusividade, os primeiros dois-pontos em **InstanceId** devem estar entre *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="15321-132">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="15321-133">Portanto, o *OrgID* não deve conter dois-pontos (': ').</span><span class="sxs-lookup"><span data-stu-id="15321-133">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="15321-134">A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos do mundo real subjacentes diferentes.</span><span class="sxs-lookup"><span data-stu-id="15321-134">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="15321-135">Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor de **InstanceId** resultante não seja reutilizado em todas as propriedades **InstanceId** produzidas por este provedor ou por outros provedores para esse namespace.</span><span class="sxs-lookup"><span data-stu-id="15321-135">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="15321-136">Para instâncias definidas pela DMTF (Distributed Management Task Force), o padrão deve ser usado com o *OrgID* definido como CIM.</span><span class="sxs-lookup"><span data-stu-id="15321-136">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15321-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15321-137">Requirements</span></span>



| <span data-ttu-id="15321-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="15321-138">Requirement</span></span> | <span data-ttu-id="15321-139">Valor</span><span class="sxs-lookup"><span data-stu-id="15321-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15321-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15321-140">Minimum supported client</span></span><br/> | <span data-ttu-id="15321-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15321-141">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="15321-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15321-142">Minimum supported server</span></span><br/> | <span data-ttu-id="15321-143">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15321-143">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="15321-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="15321-144">Namespace</span></span><br/>                | <span data-ttu-id="15321-145">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="15321-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15321-146">MOF</span><span class="sxs-lookup"><span data-stu-id="15321-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15321-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15321-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15321-148">DLL</span><span class="sxs-lookup"><span data-stu-id="15321-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15321-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15321-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

