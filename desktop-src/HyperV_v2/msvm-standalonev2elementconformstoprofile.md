---
description: Define os perfis registrados para os quais o sistema autônomo referenciado está em conformidade.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Classe Msvm_StandaloneV2ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921257"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a><span data-ttu-id="d8b48-103">\_Classe Msvm StandaloneV2ElementConformsToProfile</span><span class="sxs-lookup"><span data-stu-id="d8b48-103">Msvm\_StandaloneV2ElementConformsToProfile class</span></span>

<span data-ttu-id="d8b48-104">Define os perfis registrados para os quais o sistema autônomo referenciado está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8b48-104">Defines the registered profiles to which the referenced standalone system conforms.</span></span>

<span data-ttu-id="d8b48-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d8b48-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b48-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8b48-106">Syntax</span></span>

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="d8b48-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d8b48-107">Members</span></span>

<span data-ttu-id="d8b48-108">A classe **Msvm \_ StandaloneV2ElementConformsToProfile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d8b48-108">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="d8b48-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8b48-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8b48-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8b48-110">Properties</span></span>

<span data-ttu-id="d8b48-111">A classe **Msvm \_ StandaloneV2ElementConformsToProfile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d8b48-111">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8b48-112">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="d8b48-112">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8b48-113">Tipo de dados: **Msvm \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="d8b48-113">Data type: **Msvm\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="d8b48-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8b48-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8b48-115">Qualificadores: [ **substituição**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d8b48-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d8b48-116">O perfil registrado no qual o sistema autônomo está de acordo.</span><span class="sxs-lookup"><span data-stu-id="d8b48-116">The registered profile to which the standalone system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="d8b48-117">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="d8b48-117">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8b48-118">Tipo de dados: **Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="d8b48-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d8b48-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8b48-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8b48-120">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT \_ targetNamespace** (" \\ \\ virtualização de raiz \\ \\ v2")</span><span class="sxs-lookup"><span data-stu-id="d8b48-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT\_TargetNamespace** ("root\\\\virtualization\\\\v2")</span></span>
</dt> </dl>

<span data-ttu-id="d8b48-121">O sistema autônomo que está em conformidade com o perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="d8b48-121">The standalone system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8b48-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8b48-122">Requirements</span></span>



| <span data-ttu-id="d8b48-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8b48-123">Requirement</span></span> | <span data-ttu-id="d8b48-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d8b48-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b48-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8b48-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b48-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d8b48-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d8b48-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8b48-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b48-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d8b48-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d8b48-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8b48-129">Namespace</span></span><br/>                | <span data-ttu-id="d8b48-130">\\Interoperabilidade raiz</span><span class="sxs-lookup"><span data-stu-id="d8b48-130">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="d8b48-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d8b48-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8b48-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8b48-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8b48-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d8b48-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8b48-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8b48-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8b48-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8b48-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b48-136">**Msvm \_ ElementConformsToProfile**</span><span class="sxs-lookup"><span data-stu-id="d8b48-136">**Msvm\_ElementConformsToProfile**</span></span>](msvm-elementconformstoprofile.md)
</dt> </dl>

 

