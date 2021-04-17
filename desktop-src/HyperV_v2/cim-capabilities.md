---
description: Uma classe abstrata para subclasses que descreve as capacidades de um elemento gerenciado associado e o potencial das habilidades.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: Classe CIM_Capabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e08fcef34c8c2e932851fb428fd32533eee4877e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787117"
---
# <a name="cim_capabilities-class"></a><span data-ttu-id="8f08a-103">\_Classe de recursos CIM</span><span class="sxs-lookup"><span data-stu-id="8f08a-103">CIM\_Capabilities class</span></span>

<span data-ttu-id="8f08a-104">Uma classe abstrata para subclasses que descreve as capacidades de um elemento gerenciado associado e o potencial das habilidades.</span><span class="sxs-lookup"><span data-stu-id="8f08a-104">An abstract class for subclasses that describes the abilities of an associated managed element, and the potential of the abilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f08a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f08a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="8f08a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="8f08a-106">Members</span></span>

<span data-ttu-id="8f08a-107">A classe de **\_ recursos CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8f08a-107">The **CIM\_Capabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="8f08a-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f08a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f08a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f08a-109">Properties</span></span>

<span data-ttu-id="8f08a-110">A classe de **\_ recursos CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8f08a-110">The **CIM\_Capabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f08a-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8f08a-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f08a-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f08a-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f08a-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f08a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f08a-114">Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="8f08a-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="8f08a-115">O nome amigável do usuário para esta instância de classe.</span><span class="sxs-lookup"><span data-stu-id="8f08a-115">The user friendly name for this class instance.</span></span> <span data-ttu-id="8f08a-116">Além disso, o nome amigável do usuário pode ser usado como uma propriedade de índice para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="8f08a-116">In addition, the user friendly name can be used as a index property for a query.</span></span> <span data-ttu-id="8f08a-117">Esse valor não precisa ser exclusivo em seu namespace.</span><span class="sxs-lookup"><span data-stu-id="8f08a-117">This value does not have to be unique within its namespace.</span></span>

</dd> <dt>

<span data-ttu-id="8f08a-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8f08a-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f08a-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f08a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f08a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f08a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f08a-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="8f08a-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="8f08a-122">Identifica exclusivamente e de forma opaca uma instância dessa classe dentro do escopo do namespace que a contém.</span><span class="sxs-lookup"><span data-stu-id="8f08a-122">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="8f08a-123">Para garantir a exclusividade no namespace, o valor da propriedade **InstanceId** deve ser construído no seguinte padrão: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="8f08a-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="8f08a-124">*OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que define a **InstanceId** ou ser uma ID registrada que é atribuída por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="8f08a-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="8f08a-125">Esse padrão é semelhante à estrutura de nomes de classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="8f08a-125">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="8f08a-126">Além disso, para garantir a exclusividade, os primeiros dois-pontos em **InstanceId** devem estar entre *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="8f08a-126">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="8f08a-127">Portanto, o *OrgID* não deve conter dois-pontos (': ').</span><span class="sxs-lookup"><span data-stu-id="8f08a-127">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="8f08a-128">A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos do mundo real subjacentes diferentes.</span><span class="sxs-lookup"><span data-stu-id="8f08a-128">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="8f08a-129">Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor de **InstanceId** resultante não seja reutilizado em todas as propriedades **InstanceId** produzidas por este provedor ou por outros provedores para esse namespace.</span><span class="sxs-lookup"><span data-stu-id="8f08a-129">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="8f08a-130">Para instâncias definidas pela DMTF (Distributed Management Task Force), o padrão deve ser usado com o *OrgID* definido como CIM.</span><span class="sxs-lookup"><span data-stu-id="8f08a-130">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f08a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f08a-131">Requirements</span></span>



| <span data-ttu-id="8f08a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f08a-132">Requirement</span></span> | <span data-ttu-id="8f08a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8f08a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f08a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f08a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8f08a-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8f08a-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8f08a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f08a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8f08a-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f08a-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8f08a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f08a-138">Namespace</span></span><br/>                | <span data-ttu-id="8f08a-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8f08a-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8f08a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8f08a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f08a-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f08a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f08a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8f08a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f08a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8f08a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8f08a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f08a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f08a-145">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="8f08a-145">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

