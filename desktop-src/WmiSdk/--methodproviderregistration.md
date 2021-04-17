---
description: Registra provedores de método com o WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: Classe __MethodProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798391"
---
# <a name="__methodproviderregistration-class"></a><span data-ttu-id="4d2b8-103">\_\_Classe MethodProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="4d2b8-103">\_\_MethodProviderRegistration class</span></span>

<span data-ttu-id="4d2b8-104">A classe de sistema **\_ \_ MethodProviderRegistration** registra provedores de método com o WMI.</span><span class="sxs-lookup"><span data-stu-id="4d2b8-104">The **\_\_MethodProviderRegistration** system class registers method providers with WMI.</span></span>

<span data-ttu-id="4d2b8-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4d2b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4d2b8-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="4d2b8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d2b8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d2b8-107">Syntax</span></span>

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="4d2b8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4d2b8-108">Members</span></span>

<span data-ttu-id="4d2b8-109">A classe **\_ \_ MethodProviderRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4d2b8-109">The **\_\_MethodProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="4d2b8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4d2b8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d2b8-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4d2b8-111">Properties</span></span>

<span data-ttu-id="4d2b8-112">A classe **\_ \_ MethodProviderRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4d2b8-112">The **\_\_MethodProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d2b8-113">**operador**</span><span class="sxs-lookup"><span data-stu-id="4d2b8-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b8-114">Tipo de dados: **\_ \_ provedor**</span><span class="sxs-lookup"><span data-stu-id="4d2b8-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b8-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d2b8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b8-116">Referência a uma instância do [**\_ \_ provedor**](--provider.md) que representa o caminho do objeto do provedor de método.</span><span class="sxs-lookup"><span data-stu-id="4d2b8-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the method provider.</span></span> <span data-ttu-id="4d2b8-117">Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4d2b8-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d2b8-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d2b8-118">Remarks</span></span>

<span data-ttu-id="4d2b8-119">A classe **\_ \_ MethodProviderRegistration** é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4d2b8-119">The **\_\_MethodProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="4d2b8-120">Somente os administradores podem registrar ou excluir um provedor de métodos criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e do **\_ \_ MethodProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="4d2b8-120">Only administrators can register or delete a method provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_MethodProviderRegistration**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d2b8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d2b8-121">Requirements</span></span>



| <span data-ttu-id="4d2b8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d2b8-122">Requirement</span></span> | <span data-ttu-id="4d2b8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4d2b8-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4d2b8-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d2b8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4d2b8-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d2b8-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4d2b8-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d2b8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4d2b8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d2b8-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4d2b8-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d2b8-128">Namespace</span></span><br/>                | <span data-ttu-id="4d2b8-129">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="4d2b8-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4d2b8-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d2b8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d2b8-131">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="4d2b8-131">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="4d2b8-132">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="4d2b8-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4d2b8-133">Registrando um provedor de métodos</span><span class="sxs-lookup"><span data-stu-id="4d2b8-133">Registering a Method Provider</span></span>](registering-a-method-provider.md)
</dt> </dl>

 

