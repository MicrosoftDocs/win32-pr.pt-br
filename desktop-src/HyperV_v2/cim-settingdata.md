---
description: Representa parâmetros operacionais e de configuração para \_ instâncias de CIM managedelement.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: Classe CIM_SettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 934aaaf694a79537f5761717f91db398141c33d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170068"
---
# <a name="cim_settingdata-class"></a><span data-ttu-id="84328-103">Classe do CIM \_ SettingData</span><span class="sxs-lookup"><span data-stu-id="84328-103">CIM\_SettingData class</span></span>

<span data-ttu-id="84328-104">Representa parâmetros operacionais e de configuração para instâncias de [**CIM \_ managedelement**](cim-managedelement.md) .</span><span class="sxs-lookup"><span data-stu-id="84328-104">Represents configuration and operational parameters for [**CIM\_ManagedElement**](cim-managedelement.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="84328-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84328-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="84328-106">Membros</span><span class="sxs-lookup"><span data-stu-id="84328-106">Members</span></span>

<span data-ttu-id="84328-107">A classe do **CIM \_ SettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="84328-107">The **CIM\_SettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="84328-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="84328-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84328-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="84328-109">Properties</span></span>

<span data-ttu-id="84328-110">A classe **CIM \_ SettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="84328-110">The **CIM\_SettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84328-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="84328-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84328-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="84328-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84328-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="84328-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84328-114">Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="84328-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="84328-115">O nome amigável para uma instância desta classe.</span><span class="sxs-lookup"><span data-stu-id="84328-115">The user-friendly name for an instance of this class.</span></span> <span data-ttu-id="84328-116">Além disso, o nome amigável do usuário pode ser usado como um índice para uma pesquisa ou consulta.</span><span class="sxs-lookup"><span data-stu-id="84328-116">In addition, the user-friendly name can be used as an index for a search or query.</span></span> <span data-ttu-id="84328-117">O nome não precisa ser exclusivo em um namespace.</span><span class="sxs-lookup"><span data-stu-id="84328-117">The name does not have to be unique within a namespace.</span></span>

</dd> <dt>

<span data-ttu-id="84328-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84328-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84328-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="84328-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84328-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="84328-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84328-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="84328-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="84328-122">Identifica exclusivamente uma instância dessa classe dentro do escopo do namespace que a contém.</span><span class="sxs-lookup"><span data-stu-id="84328-122">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="84328-123">Para garantir a exclusividade no namespace, o valor da propriedade **InstanceId** deve ser construído no seguinte padrão: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="84328-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="84328-124">*OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que define a propriedade **InstanceId** ou ser uma ID registrada que é atribuída por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="84328-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="84328-125">*OrgID* não deve conter dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="84328-125">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="84328-126">Os primeiros dois-pontos em **InstanceId** devem estar entre *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="84328-126">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="84328-127">A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos do mundo real subjacentes diferentes.</span><span class="sxs-lookup"><span data-stu-id="84328-127">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="84328-128">Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor de **InstanceId** resultante não seja reutilizado em todas as propriedades **InstanceId** produzidas por este provedor ou por outros provedores para esse namespace.</span><span class="sxs-lookup"><span data-stu-id="84328-128">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="84328-129">Para instâncias definidas por DMTF, o padrão deve ser usado com o *OrgID* definido como "CIM".</span><span class="sxs-lookup"><span data-stu-id="84328-129">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84328-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84328-130">Requirements</span></span>



| <span data-ttu-id="84328-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="84328-131">Requirement</span></span> | <span data-ttu-id="84328-132">Valor</span><span class="sxs-lookup"><span data-stu-id="84328-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84328-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84328-133">Minimum supported client</span></span><br/> | <span data-ttu-id="84328-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="84328-134">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="84328-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84328-135">Minimum supported server</span></span><br/> | <span data-ttu-id="84328-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84328-136">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="84328-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="84328-137">Namespace</span></span><br/>                | <span data-ttu-id="84328-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="84328-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="84328-139">MOF</span><span class="sxs-lookup"><span data-stu-id="84328-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84328-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84328-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84328-141">DLL</span><span class="sxs-lookup"><span data-stu-id="84328-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84328-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84328-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84328-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="84328-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84328-144">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="84328-144">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

