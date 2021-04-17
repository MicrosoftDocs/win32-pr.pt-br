---
description: Usado para registrar provedores de eventos com Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: Classe __EventProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811495"
---
# <a name="__eventproviderregistration-class"></a><span data-ttu-id="4ab0c-103">\_\_Classe EventProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="4ab0c-103">\_\_EventProviderRegistration class</span></span>

<span data-ttu-id="4ab0c-104">A classe de sistema **\_ \_ EventProviderRegistration** é usada para registrar provedores de eventos com instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4ab0c-104">The **\_\_EventProviderRegistration** system class is used to register event providers with Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="4ab0c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4ab0c-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ab0c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ab0c-107">Syntax</span></span>

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="4ab0c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4ab0c-108">Members</span></span>

<span data-ttu-id="4ab0c-109">A classe **\_ \_ EventProviderRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4ab0c-109">The **\_\_EventProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="4ab0c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ab0c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ab0c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ab0c-111">Properties</span></span>

<span data-ttu-id="4ab0c-112">A classe **\_ \_ EventProviderRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-112">The **\_\_EventProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ab0c-113">**EventQueryList**</span><span class="sxs-lookup"><span data-stu-id="4ab0c-113">**EventQueryList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ab0c-114">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ab0c-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4ab0c-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ab0c-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4ab0c-116">Uma ou mais consultas WQL (linguagem de consulta Instrumentação de Gerenciamento do Windows) que descrevem os eventos aos quais o provedor de eventos dá suporte.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-116">One or more Windows Management Instrumentation Query Language (WQL) queries that describe the events that the event provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="4ab0c-117">**operador**</span><span class="sxs-lookup"><span data-stu-id="4ab0c-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ab0c-118">Tipo de dados: **\_ \_ provedor**</span><span class="sxs-lookup"><span data-stu-id="4ab0c-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="4ab0c-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ab0c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ab0c-120">Caminho do objeto para o provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-120">Object path to the event provider.</span></span> <span data-ttu-id="4ab0c-121">Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4ab0c-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ab0c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ab0c-122">Remarks</span></span>

<span data-ttu-id="4ab0c-123">Somente os administradores podem registrar ou excluir um provedor de eventos criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e do [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4ab0c-123">Only administrators can register or delete an event provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="4ab0c-124">A classe **\_ \_ EventProviderRegistration** é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4ab0c-124">The **\_\_EventProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ab0c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ab0c-125">Requirements</span></span>



| <span data-ttu-id="4ab0c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ab0c-126">Requirement</span></span> | <span data-ttu-id="4ab0c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4ab0c-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4ab0c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ab0c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4ab0c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ab0c-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4ab0c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ab0c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4ab0c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ab0c-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4ab0c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ab0c-132">Namespace</span></span><br/>                | <span data-ttu-id="4ab0c-133">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="4ab0c-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4ab0c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ab0c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ab0c-135">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="4ab0c-135">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="4ab0c-136">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="4ab0c-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4ab0c-137">Registrando um provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="4ab0c-137">Registering an Event Provider</span></span>](registering-an-event-provider.md)
</dt> <dt>

[<span data-ttu-id="4ab0c-138">Escrevendo um provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="4ab0c-138">Writing an Event Provider</span></span>](writing-an-event-provider.md)
</dt> </dl>

 

