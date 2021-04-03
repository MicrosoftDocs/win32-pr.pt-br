---
description: É uma classe base abstrata que é usada no registro de um consumidor de evento permanente.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: Classe __EventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922877"
---
# <a name="__eventconsumer-class"></a><span data-ttu-id="27689-103">\_\_Classe EventConsumer</span><span class="sxs-lookup"><span data-stu-id="27689-103">\_\_EventConsumer class</span></span>

<span data-ttu-id="27689-104">A classe de sistema **\_ \_ EventConsumer** é uma classe base abstrata que é usada no registro de um consumidor de evento permanente.</span><span class="sxs-lookup"><span data-stu-id="27689-104">The **\_\_EventConsumer** system class is an abstract base class that is used in the registration of a permanent event consumer.</span></span> <span data-ttu-id="27689-105">Você pode derivar uma nova classe de consumidor de eventos de **\_ \_ EventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="27689-105">You can derive a new event consumer class from **\_\_EventConsumer**.</span></span>

<span data-ttu-id="27689-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="27689-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="27689-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="27689-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="27689-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27689-108">Syntax</span></span>

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a><span data-ttu-id="27689-109">Membros</span><span class="sxs-lookup"><span data-stu-id="27689-109">Members</span></span>

<span data-ttu-id="27689-110">A classe **\_ \_ EventConsumer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="27689-110">The **\_\_EventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="27689-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="27689-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27689-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="27689-112">Properties</span></span>

<span data-ttu-id="27689-113">A classe **\_ \_ EventConsumer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="27689-113">The **\_\_EventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27689-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="27689-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27689-115">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="27689-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="27689-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="27689-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27689-117">SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro.</span><span class="sxs-lookup"><span data-stu-id="27689-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="27689-118">O WMI armazena o SID do usuário que cria uma instância de **\_ \_ EventConsumer** ou o SID do administrador, dependendo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="27689-118">WMI stores the SID of the user who creates an instance of **\_\_EventConsumer** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="27689-119">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="27689-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="27689-120">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="27689-120">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27689-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="27689-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27689-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="27689-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27689-123">Nome do computador ao qual Instrumentação de Gerenciamento do Windows (WMI) envia eventos.</span><span class="sxs-lookup"><span data-stu-id="27689-123">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

</dd> <dt>

<span data-ttu-id="27689-124">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="27689-124">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27689-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27689-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27689-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="27689-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27689-127">Fila máxima para um consumidor específico, em bytes.</span><span class="sxs-lookup"><span data-stu-id="27689-127">Maximum queue for a specific consumer, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27689-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="27689-128">Remarks</span></span>

<span data-ttu-id="27689-129">A classe **\_ \_ EventConsumer** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md), que não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="27689-129">The **\_\_EventConsumer** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which does not have properties.</span></span>

<span data-ttu-id="27689-130">Os consumidores permanentes definem novas classes de consumidor para descrever uma ação a ser tomada e os dados a serem processados quando os consumidores recebem notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="27689-130">Permanent consumers define new consumer classes to describe an action to take and data to be processed when consumers receive event notifications.</span></span> <span data-ttu-id="27689-131">Os consumidores permanentes têm preocupações especiais de segurança.</span><span class="sxs-lookup"><span data-stu-id="27689-131">Permanent consumers have special security concerns.</span></span> <span data-ttu-id="27689-132">Para obter mais informações, consulte [SECURING WMI Events](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="27689-132">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27689-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27689-133">Requirements</span></span>



| <span data-ttu-id="27689-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="27689-134">Requirement</span></span> | <span data-ttu-id="27689-135">Valor</span><span class="sxs-lookup"><span data-stu-id="27689-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="27689-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27689-136">Minimum supported client</span></span><br/> | <span data-ttu-id="27689-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27689-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="27689-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27689-138">Minimum supported server</span></span><br/> | <span data-ttu-id="27689-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27689-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="27689-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="27689-140">Namespace</span></span><br/>                | <span data-ttu-id="27689-141">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="27689-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="27689-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="27689-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27689-143">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="27689-143">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="27689-144">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="27689-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="27689-145">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="27689-145">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="27689-146">Criando uma nova classe de consumidor de evento permanente</span><span class="sxs-lookup"><span data-stu-id="27689-146">Creating a New Permanent Event Consumer Class</span></span>](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[<span data-ttu-id="27689-147">Criando um consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="27689-147">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="27689-148">Protegendo eventos WMI</span><span class="sxs-lookup"><span data-stu-id="27689-148">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

