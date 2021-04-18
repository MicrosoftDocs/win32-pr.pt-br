---
description: Relata um evento de criação de namespace, que é um tipo de evento intrínseco gerado quando um novo namespace é adicionado ao namespace atual.
ms.assetid: 50b9860a-d6e8-4dab-a7d0-09da9dd37b6b
ms.tgt_platform: multiple
title: Classe __NamespaceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 8432bcfb2c96c70b91a7f0d187297217082e2d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810275"
---
# <a name="__namespacecreationevent-class"></a><span data-ttu-id="5e645-103">\_\_Classe NamespaceCreationEvent</span><span class="sxs-lookup"><span data-stu-id="5e645-103">\_\_NamespaceCreationEvent class</span></span>

<span data-ttu-id="5e645-104">A classe de sistema **\_ \_ NamespaceCreationEvent** relata um evento de criação de namespace, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) gerado quando um novo namespace é adicionado ao namespace atual.</span><span class="sxs-lookup"><span data-stu-id="5e645-104">The **\_\_NamespaceCreationEvent** system class reports a namespace creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new namespace is added to the current namespace.</span></span>

<span data-ttu-id="5e645-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5e645-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5e645-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5e645-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e645-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e645-107">Syntax</span></span>

``` syntax
class __NamespaceCreationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="5e645-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5e645-108">Members</span></span>

<span data-ttu-id="5e645-109">A classe **\_ \_ NamespaceCreationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5e645-109">The **\_\_NamespaceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="5e645-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e645-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e645-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e645-111">Properties</span></span>

<span data-ttu-id="5e645-112">A classe **\_ \_ NamespaceCreationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5e645-112">The **\_\_NamespaceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e645-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="5e645-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e645-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="5e645-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5e645-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e645-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e645-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="5e645-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="5e645-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="5e645-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e645-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="5e645-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e645-119">Tipo de dados: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="5e645-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="5e645-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e645-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e645-121">Cópia da instância de [**\_ \_ namespace**](--namespace.md) que foi criada.</span><span class="sxs-lookup"><span data-stu-id="5e645-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that was created.</span></span> <span data-ttu-id="5e645-122">A propriedade **Name** da instância do **\_ \_ namespace** indica qual namespace foi criado.</span><span class="sxs-lookup"><span data-stu-id="5e645-122">The **Name** property of the **\_\_Namespace** instance indicates which namespace was created.</span></span> <span data-ttu-id="5e645-123">Essa propriedade é herdada de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="5e645-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e645-124">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="5e645-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e645-125">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5e645-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e645-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e645-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e645-127">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="5e645-127">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="5e645-128">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="5e645-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="5e645-129">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="5e645-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="5e645-130">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="5e645-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="5e645-131">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5e645-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e645-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e645-132">Remarks</span></span>

<span data-ttu-id="5e645-133">A classe **\_ \_ NamespaceCreationEvent** é derivada de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="5e645-133">The **\_\_NamespaceCreationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e645-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e645-134">Requirements</span></span>



| <span data-ttu-id="5e645-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e645-135">Requirement</span></span> | <span data-ttu-id="5e645-136">Valor</span><span class="sxs-lookup"><span data-stu-id="5e645-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5e645-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e645-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5e645-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e645-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5e645-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e645-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5e645-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e645-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5e645-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e645-141">Namespace</span></span><br/>                | <span data-ttu-id="5e645-142">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="5e645-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5e645-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e645-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e645-144">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="5e645-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="5e645-145">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="5e645-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

