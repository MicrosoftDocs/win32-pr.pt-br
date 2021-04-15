---
description: Registra provedores de propriedade no WMI.
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: Classe __PropertyProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505945"
---
# <a name="__propertyproviderregistration-class"></a><span data-ttu-id="ea805-103">\_\_Classe PropertyProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="ea805-103">\_\_PropertyProviderRegistration class</span></span>

<span data-ttu-id="ea805-104">A classe de sistema **\_ \_ PropertyProviderRegistration** registra os provedores de propriedade no WMI.</span><span class="sxs-lookup"><span data-stu-id="ea805-104">The **\_\_PropertyProviderRegistration** system class registers property providers in WMI.</span></span>

<span data-ttu-id="ea805-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ea805-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ea805-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ea805-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea805-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea805-107">Syntax</span></span>

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a><span data-ttu-id="ea805-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ea805-108">Members</span></span>

<span data-ttu-id="ea805-109">A classe **\_ \_ PropertyProviderRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ea805-109">The **\_\_PropertyProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="ea805-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea805-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea805-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea805-111">Properties</span></span>

<span data-ttu-id="ea805-112">A classe **\_ \_ PropertyProviderRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ea805-112">The **\_\_PropertyProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea805-113">**operador**</span><span class="sxs-lookup"><span data-stu-id="ea805-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea805-114">Tipo de dados: **\_ \_ provedor**</span><span class="sxs-lookup"><span data-stu-id="ea805-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="ea805-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea805-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea805-116">Referência a uma instância do [**\_ \_ provedor**](--provider.md) que representa o caminho do objeto do provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ea805-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the property provider.</span></span> <span data-ttu-id="ea805-117">Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="ea805-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea805-118">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="ea805-118">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea805-119">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea805-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea805-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ea805-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ea805-121">Descreve se o provedor de classe ou instância dá suporte à recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="ea805-121">Describes whether the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="ea805-122">True</span><span class="sxs-lookup"><span data-stu-id="ea805-122">True</span></span>
</dt> <dd>

<span data-ttu-id="ea805-123">O provedor dá suporte à recuperação de dados implementando [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="ea805-123">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="ea805-124">Falso</span><span class="sxs-lookup"><span data-stu-id="ea805-124">False</span></span>
</dt> <dd>

<span data-ttu-id="ea805-125">O provedor não dá suporte à recuperação de dados e retorna **o \_ provedor WBEM e \_ não é \_ \_ capaz** de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="ea805-125">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ea805-126">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="ea805-126">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea805-127">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea805-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea805-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ea805-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ea805-129">Descreve se o provedor de classe ou instância dá suporte à modificação de dados.</span><span class="sxs-lookup"><span data-stu-id="ea805-129">Describes whether the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="ea805-130">True</span><span class="sxs-lookup"><span data-stu-id="ea805-130">True</span></span>
</dt> <dd>

<span data-ttu-id="ea805-131">O provedor dá suporte à modificação de classe ou instância implementando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="ea805-131">The provider supports class or instance modification by implementing one of the following methods:</span></span>

-   <span data-ttu-id="ea805-132">[**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provedores de classe)</span><span class="sxs-lookup"><span data-stu-id="ea805-132">[**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers)</span></span>
-   <span data-ttu-id="ea805-133">[**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provedores de classe)</span><span class="sxs-lookup"><span data-stu-id="ea805-133">[**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers)</span></span>

</dd> <dt>

<span data-ttu-id="ea805-134">Falso</span><span class="sxs-lookup"><span data-stu-id="ea805-134">False</span></span>
</dt> <dd>

<span data-ttu-id="ea805-135">O provedor não dá suporte à modificação de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ compatível** com [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="ea805-135">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea805-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea805-136">Remarks</span></span>

<span data-ttu-id="ea805-137">A classe **\_ \_ PropertyProviderRegistration** é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="ea805-137">The **\_\_PropertyProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="ea805-138">Somente os administradores podem registrar um provedor de propriedades criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e do **\_ \_ PropertyProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="ea805-138">Only administrators can register a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_PropertyProviderRegistration**.</span></span> <span data-ttu-id="ea805-139">Somente os administradores podem excluir um provedor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ea805-139">Only administrators can delete a property provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea805-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea805-140">Requirements</span></span>



| <span data-ttu-id="ea805-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea805-141">Requirement</span></span> | <span data-ttu-id="ea805-142">Valor</span><span class="sxs-lookup"><span data-stu-id="ea805-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ea805-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea805-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ea805-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea805-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ea805-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea805-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ea805-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea805-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ea805-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea805-147">Namespace</span></span><br/>                | <span data-ttu-id="ea805-148">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="ea805-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ea805-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea805-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea805-150">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="ea805-150">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="ea805-151">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="ea805-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="ea805-152">Registrando um provedor de propriedades</span><span class="sxs-lookup"><span data-stu-id="ea805-152">Registering a Property Provider</span></span>](registering-a-property-provider.md)
</dt> </dl>

 

