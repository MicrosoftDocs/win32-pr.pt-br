---
description: Relata um evento de modificação de namespace, que é um tipo de evento intrínseco que é gerado quando um namespace é modificado.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: Classe __NamespaceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663136"
---
# <a name="__namespacemodificationevent-class"></a><span data-ttu-id="8f778-103">\_\_Classe NamespaceModificationEvent</span><span class="sxs-lookup"><span data-stu-id="8f778-103">\_\_NamespaceModificationEvent class</span></span>

<span data-ttu-id="8f778-104">A classe de sistema **\_ \_ NamespaceModificationEvent** relata um evento de modificação de namespace, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que é gerado quando um namespace é modificado.</span><span class="sxs-lookup"><span data-stu-id="8f778-104">The **\_\_NamespaceModificationEvent** system class reports a namespace modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a namespace is modified.</span></span>

<span data-ttu-id="8f778-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8f778-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8f778-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8f778-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f778-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f778-107">Syntax</span></span>

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="8f778-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8f778-108">Members</span></span>

<span data-ttu-id="8f778-109">A classe **\_ \_ NamespaceModificationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8f778-109">The **\_\_NamespaceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="8f778-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f778-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f778-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f778-111">Properties</span></span>

<span data-ttu-id="8f778-112">A classe **\_ \_ NamespaceModificationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8f778-112">The **\_\_NamespaceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f778-113">**PreviousNamespace**</span><span class="sxs-lookup"><span data-stu-id="8f778-113">**PreviousNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f778-114">Tipo de dados: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="8f778-114">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="8f778-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f778-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f778-116">Cópia da versão original de uma instância de [**\_ \_ namespace**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="8f778-116">Copy of the original version of a [**\_\_Namespace**](--namespace.md) instance.</span></span> <span data-ttu-id="8f778-117">A propriedade **Name** dessa instância identifica o namespace que é modificado.</span><span class="sxs-lookup"><span data-stu-id="8f778-117">The **Name** property of this instance identifies the namespace that is modified.</span></span>

</dd> <dt>

<span data-ttu-id="8f778-118">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="8f778-118">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f778-119">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="8f778-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8f778-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f778-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f778-121">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="8f778-121">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="8f778-122">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8f778-122">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f778-123">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="8f778-123">**SECURITY\_DESCRIPTOR**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f778-124">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="8f778-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8f778-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f778-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f778-126">Descritor que o provedor de eventos usa para determinar os usuários que podem receber um evento.</span><span class="sxs-lookup"><span data-stu-id="8f778-126">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="8f778-127">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8f778-127">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="8f778-128">Uma  ACL (lista de controle de acesso) nula [**no \_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado a todas as pessoas o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="8f778-128">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="8f778-129">Para obter mais informações, consulte [criando um descritor de segurança para um novo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="8f778-129">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="8f778-130">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="8f778-130">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f778-131">Tipo de dados: **\_ \_ namespace**</span><span class="sxs-lookup"><span data-stu-id="8f778-131">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="8f778-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f778-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f778-133">Cópia da instância de [**\_ \_ namespace**](--namespace.md) que é modificada.</span><span class="sxs-lookup"><span data-stu-id="8f778-133">Copy of the [**\_\_Namespace**](--namespace.md) instance that is modified.</span></span> <span data-ttu-id="8f778-134">A propriedade **Name** da instância do **\_ \_ namespace** indica o namespace que é modificado.</span><span class="sxs-lookup"><span data-stu-id="8f778-134">The **Name** property of the **\_\_Namespace** instance indicates the namespace that is modified.</span></span> <span data-ttu-id="8f778-135">Essa propriedade é herdada da classe [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="8f778-135">This property is inherited from class [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f778-136">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="8f778-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f778-137">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f778-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f778-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f778-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f778-139">Valor exclusivo que indica a hora em que um evento é gerado.</span><span class="sxs-lookup"><span data-stu-id="8f778-139">Unique value that indicates the time that an event is generated.</span></span> <span data-ttu-id="8f778-140">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="8f778-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="8f778-141">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="8f778-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="8f778-142">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8f778-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="8f778-143">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f778-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f778-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f778-144">Remarks</span></span>

<span data-ttu-id="8f778-145">A classe **\_ \_ NamespaceModificationEvent** é derivada de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="8f778-145">The **\_\_NamespaceModificationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

<span data-ttu-id="8f778-146">As únicas diferenças entre o namespace de destino e o namespace anterior são os qualificadores e propriedades, exceto [**Name**](--namespace.md).</span><span class="sxs-lookup"><span data-stu-id="8f778-146">The only differences between the target namespace and the previous namespace is the qualifiers and properties except [**Name**](--namespace.md).</span></span>

<span data-ttu-id="8f778-147">Observe que a propriedade [**Name**](--namespace.md) de uma instância de **\_ \_ namespace** não pode ser alterada porque namespaces não podem ser renomeados.</span><span class="sxs-lookup"><span data-stu-id="8f778-147">Note that the [**Name**](--namespace.md) property of a **\_\_Namespace** instance cannot change because namespaces cannot be renamed.</span></span> <span data-ttu-id="8f778-148">Para modificar o nome de um namespace, a instância do **\_ \_ namespace** deve ser excluída e recriada com um novo nome.</span><span class="sxs-lookup"><span data-stu-id="8f778-148">To modify the name of a namespace, the **\_\_Namespace** instance must be deleted and re-created with a new name.</span></span> <span data-ttu-id="8f778-149">Portanto, os eventos de modificação de namespace são gerados quando uma alteração ocorre em qualificadores e propriedades diferentes de **Name**.</span><span class="sxs-lookup"><span data-stu-id="8f778-149">Therefore, namespace modification events are generated when a change occurs to qualifiers and properties other than **Name**.</span></span> <span data-ttu-id="8f778-150">Um evento de modificação de namespace não é gerado quando ocorre algum tipo de alteração no namespace.</span><span class="sxs-lookup"><span data-stu-id="8f778-150">A namespace modification event is not generated when any kind of change occurs within the namespace.</span></span> <span data-ttu-id="8f778-151">Um evento de modificação de namespace é gerado somente quando uma instância de namespace é modificada.</span><span class="sxs-lookup"><span data-stu-id="8f778-151">A namespace modification event is generated only when a namespace instance is modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f778-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f778-152">Requirements</span></span>



| <span data-ttu-id="8f778-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f778-153">Requirement</span></span> | <span data-ttu-id="8f778-154">Valor</span><span class="sxs-lookup"><span data-stu-id="8f778-154">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8f778-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f778-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8f778-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f778-156">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8f778-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f778-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8f778-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f778-158">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8f778-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f778-159">Namespace</span></span><br/>                | <span data-ttu-id="8f778-160">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="8f778-160">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8f778-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f778-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f778-162">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="8f778-162">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="8f778-163">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8f778-163">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

