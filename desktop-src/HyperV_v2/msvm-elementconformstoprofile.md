---
description: Define os perfis registrados aos quais o sistema referenciado está em conformidade.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e9b4e257c2ebc0584a8291461439f75238599d35
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843277"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="f598e-103">Classe \_ ElementConformsToProfile Msvm</span><span class="sxs-lookup"><span data-stu-id="f598e-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="f598e-104">Define os perfis registrados aos quais o sistema referenciado está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="f598e-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="f598e-105">Essa associação pode se aplicar a qualquer elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f598e-105">This association may apply to any managed element.</span></span> <span data-ttu-id="f598e-106">O uso típico o aplicará a uma instância de nível superior, como um Sistema, Namespace ou Serviço.</span><span class="sxs-lookup"><span data-stu-id="f598e-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="f598e-107">Quando aplicada a uma instância de nível superior, todas as partes constituintes devem se comportar adequadamente em suporte à conformidade do elemento gerenciado com o perfil registrado nomeado.</span><span class="sxs-lookup"><span data-stu-id="f598e-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="f598e-108">A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f598e-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f598e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f598e-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="f598e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f598e-110">Members</span></span>

<span data-ttu-id="f598e-111">A **classe \_ ElementConformsToProfile Msvm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f598e-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="f598e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f598e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f598e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f598e-113">Properties</span></span>

<span data-ttu-id="f598e-114">A **classe \_ ElementConformsToProfile Msvm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f598e-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f598e-115">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="f598e-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f598e-116">Tipo de dados: **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="f598e-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f598e-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f598e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f598e-118">Qualificadores: [ **Substituir**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f598e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f598e-119">Uma referência a uma instância da [**classe Msvm \_ RegisteredProfile**](msvm-registeredprofile.md) que representa o perfil registrado ao qual o sistema está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="f598e-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="f598e-120">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="f598e-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f598e-121">Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="f598e-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f598e-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f598e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f598e-123">Qualificadores: [ **Substituir**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f598e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f598e-124">Uma referência a uma instância da [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema que está em conformidade com o perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="f598e-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f598e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f598e-125">Requirements</span></span>



| <span data-ttu-id="f598e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f598e-126">Requirement</span></span> | <span data-ttu-id="f598e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f598e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f598e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f598e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f598e-129">Windows 8.1 \[ aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f598e-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f598e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f598e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f598e-131">Somente aplicativos da área de trabalho do Windows Server 2012 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="f598e-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f598e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f598e-132">Namespace</span></span><br/>                | <span data-ttu-id="f598e-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f598e-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f598e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f598e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f598e-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f598e-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f598e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f598e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f598e-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f598e-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

