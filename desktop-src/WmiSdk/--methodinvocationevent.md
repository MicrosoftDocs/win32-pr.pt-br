---
description: A \_ \_ classe de sistema MethodInvocationEvent está definida, mas não está implementada.
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: Classe __MethodInvocationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170624"
---
# <a name="__methodinvocationevent-class"></a><span data-ttu-id="1f70d-103">\_\_Classe MethodInvocationEvent</span><span class="sxs-lookup"><span data-stu-id="1f70d-103">\_\_MethodInvocationEvent class</span></span>

<span data-ttu-id="1f70d-104">A classe de sistema **\_ \_ MethodInvocationEvent** está definida, mas não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1f70d-104">The **\_\_MethodInvocationEvent** system class is defined but is not implemented.</span></span>

<span data-ttu-id="1f70d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1f70d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1f70d-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1f70d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f70d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f70d-107">Syntax</span></span>

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="1f70d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1f70d-108">Members</span></span>

<span data-ttu-id="1f70d-109">A classe **\_ \_ MethodInvocationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1f70d-109">The **\_\_MethodInvocationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="1f70d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f70d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f70d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f70d-111">Properties</span></span>

<span data-ttu-id="1f70d-112">A classe **\_ \_ MethodInvocationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1f70d-112">The **\_\_MethodInvocationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f70d-113">**Método**</span><span class="sxs-lookup"><span data-stu-id="1f70d-113">**Method**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f70d-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f70d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f70d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f70d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f70d-116">Método invocado para disparar o evento.</span><span class="sxs-lookup"><span data-stu-id="1f70d-116">Method invoked to trigger the event.</span></span>

</dd> <dt>

<span data-ttu-id="1f70d-117">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="1f70d-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f70d-118">Tipo de dados: **\_ \_ parâmetros**</span><span class="sxs-lookup"><span data-stu-id="1f70d-118">Data type: **\_\_Parameters**</span></span>
</dt> <dt>

<span data-ttu-id="1f70d-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f70d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f70d-120">Referência a uma instância que representa os parâmetros de entrada e saída da chamada de método.</span><span class="sxs-lookup"><span data-stu-id="1f70d-120">Reference to an instance that represents the input and output parameters of the method call.</span></span>

</dd> <dt>

<span data-ttu-id="1f70d-121">**Prechamar**</span><span class="sxs-lookup"><span data-stu-id="1f70d-121">**PreCall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f70d-122">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1f70d-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f70d-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f70d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f70d-124">Se **for true**, o evento será gerado antes que o método seja chamado.</span><span class="sxs-lookup"><span data-stu-id="1f70d-124">If **TRUE**, the event is raised before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="1f70d-125">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="1f70d-125">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f70d-126">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="1f70d-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1f70d-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f70d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f70d-128">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="1f70d-128">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="1f70d-129">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="1f70d-129">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="1f70d-130">Para obter mais informações, consulte [descritores de segurança](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="1f70d-130">For more information, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

</dd> <dt>

<span data-ttu-id="1f70d-131">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="1f70d-131">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f70d-132">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="1f70d-132">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1f70d-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f70d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f70d-134">Instância em que o método é invocado.</span><span class="sxs-lookup"><span data-stu-id="1f70d-134">Instance the method is invoked on.</span></span> <span data-ttu-id="1f70d-135">Essa propriedade é herdada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="1f70d-135">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f70d-136">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="1f70d-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f70d-137">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f70d-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f70d-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f70d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f70d-139">Valor exclusivo que indica a hora em que um evento é gerado.</span><span class="sxs-lookup"><span data-stu-id="1f70d-139">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="1f70d-140">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="1f70d-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="1f70d-141">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="1f70d-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="1f70d-142">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="1f70d-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="1f70d-143">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1f70d-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f70d-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f70d-144">Remarks</span></span>

<span data-ttu-id="1f70d-145">A classe **\_ \_ MethodInvocationEvent** é derivada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="1f70d-145">The **\_\_MethodInvocationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f70d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f70d-146">Requirements</span></span>



| <span data-ttu-id="1f70d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f70d-147">Requirement</span></span> | <span data-ttu-id="1f70d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="1f70d-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1f70d-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f70d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1f70d-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f70d-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1f70d-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f70d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1f70d-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f70d-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1f70d-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f70d-153">Namespace</span></span><br/>                | <span data-ttu-id="1f70d-154">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="1f70d-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1f70d-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f70d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f70d-156">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="1f70d-156">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="1f70d-157">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="1f70d-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

