---
description: Serve como a classe pai para as classes de registro para vários tipos de provedores.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: Classe __ProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091682"
---
# <a name="__providerregistration-class"></a><span data-ttu-id="12101-103">\_\_Classe ProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="12101-103">\_\_ProviderRegistration class</span></span>

<span data-ttu-id="12101-104">A classe de sistema abstrata **\_ \_ ProviderRegistration** serve como a classe pai para classes de registro para vários tipos de provedores.</span><span class="sxs-lookup"><span data-stu-id="12101-104">The **\_\_ProviderRegistration** abstract system class serves as the parent class for registration classes for various types of providers.</span></span>

<span data-ttu-id="12101-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="12101-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="12101-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="12101-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12101-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12101-107">Syntax</span></span>

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="12101-108">Membros</span><span class="sxs-lookup"><span data-stu-id="12101-108">Members</span></span>

<span data-ttu-id="12101-109">A classe **\_ \_ ProviderRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12101-109">The **\_\_ProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="12101-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12101-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12101-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12101-111">Properties</span></span>

<span data-ttu-id="12101-112">A classe **\_ \_ ProviderRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="12101-112">The **\_\_ProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12101-113">**operador**</span><span class="sxs-lookup"><span data-stu-id="12101-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12101-114">Tipo de dados: **\_ \_ provedor**</span><span class="sxs-lookup"><span data-stu-id="12101-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="12101-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12101-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12101-116">Referência a uma instância do [**\_ \_ provedor**](--provider.md) que representa o caminho do objeto para o provedor.</span><span class="sxs-lookup"><span data-stu-id="12101-116">Reference to an instance of [**\_\_Provider**](--provider.md) representing the object path to the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12101-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="12101-117">Remarks</span></span>

<span data-ttu-id="12101-118">A classe **\_ \_ ProviderRegistration** é derivada de [**\_ \_ SystemClass**](--systemclass.md), que não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="12101-118">The **\_\_ProviderRegistration** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="12101-119">As instâncias da classe de sistema **\_ \_ ProviderRegistration** nunca são criadas.</span><span class="sxs-lookup"><span data-stu-id="12101-119">Instances of the **\_\_ProviderRegistration** system class are never created.</span></span> <span data-ttu-id="12101-120">As classes que os provedores usam para criar instâncias para o registro derivam direta ou indiretamente dessa classe.</span><span class="sxs-lookup"><span data-stu-id="12101-120">The classes that providers use to create instances for registration derive either directly or indirectly from this class.</span></span> <span data-ttu-id="12101-121">Essas classes são:</span><span class="sxs-lookup"><span data-stu-id="12101-121">These classes are:</span></span>

[<span data-ttu-id="12101-122">**\_\_ClassProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="12101-122">**\_\_ClassProviderRegistration**</span></span>](--classproviderregistration.md)

[<span data-ttu-id="12101-123">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="12101-123">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md)

[<span data-ttu-id="12101-124">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="12101-124">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

[<span data-ttu-id="12101-125">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="12101-125">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

[<span data-ttu-id="12101-126">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="12101-126">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

[<span data-ttu-id="12101-127">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="12101-127">**\_\_ObjectProviderRegistration**</span></span>](--objectproviderregistration.md)

[<span data-ttu-id="12101-128">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="12101-128">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

<span data-ttu-id="12101-129">Somente os administradores podem registrar ou excluir um provedor criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e registrando-o.</span><span class="sxs-lookup"><span data-stu-id="12101-129">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="12101-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12101-130">Requirements</span></span>



| <span data-ttu-id="12101-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="12101-131">Requirement</span></span> | <span data-ttu-id="12101-132">Valor</span><span class="sxs-lookup"><span data-stu-id="12101-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="12101-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12101-133">Minimum supported client</span></span><br/> | <span data-ttu-id="12101-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12101-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="12101-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12101-135">Minimum supported server</span></span><br/> | <span data-ttu-id="12101-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12101-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="12101-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="12101-137">Namespace</span></span><br/>                | <span data-ttu-id="12101-138">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="12101-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="12101-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="12101-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12101-140">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="12101-140">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="12101-141">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="12101-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="12101-142">Registrando um provedor</span><span class="sxs-lookup"><span data-stu-id="12101-142">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

