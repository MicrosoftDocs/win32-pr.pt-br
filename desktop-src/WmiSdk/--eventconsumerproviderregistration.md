---
description: Registra provedores de consumidor de eventos com o WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829508"
---
# <a name="__eventconsumerproviderregistration-class"></a><span data-ttu-id="0d0dd-103">\_\_Classe EventConsumerProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="0d0dd-103">\_\_EventConsumerProviderRegistration class</span></span>

<span data-ttu-id="0d0dd-104">A classe de sistema **\_ \_ EventConsumerProviderRegistration** registra provedores de consumidor de eventos com o WMI.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-104">The **\_\_EventConsumerProviderRegistration** system class registers event consumer providers with WMI.</span></span>

<span data-ttu-id="0d0dd-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0d0dd-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0dd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d0dd-107">Syntax</span></span>

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="0d0dd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0d0dd-108">Members</span></span>

<span data-ttu-id="0d0dd-109">A classe **\_ \_ EventConsumerProviderRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0d0dd-109">The **\_\_EventConsumerProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="0d0dd-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d0dd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d0dd-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d0dd-111">Properties</span></span>

<span data-ttu-id="0d0dd-112">A classe **\_ \_ EventConsumerProviderRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-112">The **\_\_EventConsumerProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d0dd-113">**ConsumerClassNames**</span><span class="sxs-lookup"><span data-stu-id="0d0dd-113">**ConsumerClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d0dd-114">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d0dd-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d0dd-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d0dd-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d0dd-116">Matriz de nomes das classes de consumidor lógicas às quais o provedor de consumidor de eventos dá suporte.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-116">Array of names of the logical consumer classes that the event consumer provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="0d0dd-117">**operador**</span><span class="sxs-lookup"><span data-stu-id="0d0dd-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d0dd-118">Tipo de dados: **\_ \_ provedor**</span><span class="sxs-lookup"><span data-stu-id="0d0dd-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="0d0dd-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d0dd-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d0dd-120">Caminho do objeto para o provedor.</span><span class="sxs-lookup"><span data-stu-id="0d0dd-120">Object path to the provider.</span></span> <span data-ttu-id="0d0dd-121">Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d0dd-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d0dd-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d0dd-122">Remarks</span></span>

<span data-ttu-id="0d0dd-123">A classe **\_ \_ EventConsumerProviderRegistration** é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d0dd-123">The **\_\_EventConsumerProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d0dd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d0dd-124">Requirements</span></span>



| <span data-ttu-id="0d0dd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d0dd-125">Requirement</span></span> | <span data-ttu-id="0d0dd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0d0dd-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0d0dd-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d0dd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0dd-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d0dd-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0d0dd-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d0dd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0dd-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d0dd-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0d0dd-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d0dd-131">Namespace</span></span><br/>                | <span data-ttu-id="0d0dd-132">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="0d0dd-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0d0dd-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d0dd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0dd-134">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="0d0dd-134">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="0d0dd-135">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="0d0dd-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="0d0dd-136">Registrando um provedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="0d0dd-136">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
</dt> <dt>

[<span data-ttu-id="0d0dd-137">Escrevendo um provedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="0d0dd-137">Writing an Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)
</dt> </dl>

 

