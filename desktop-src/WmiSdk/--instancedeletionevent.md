---
description: Relata um evento de exclusão de instância, que é um tipo de evento intrínseco gerado quando uma instância é excluída do namespace.
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: Classe __InstanceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797949"
---
# <a name="__instancedeletionevent-class"></a><span data-ttu-id="3de7a-103">\_\_Classe InstanceDeletionEvent</span><span class="sxs-lookup"><span data-stu-id="3de7a-103">\_\_InstanceDeletionEvent class</span></span>

<span data-ttu-id="3de7a-104">A classe de sistema **\_ \_ InstanceDeletionEvent** relata um evento de exclusão de instância, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) gerado quando uma instância é excluída do namespace.</span><span class="sxs-lookup"><span data-stu-id="3de7a-104">The **\_\_InstanceDeletionEvent** system class reports an instance deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance is deleted from the namespace.</span></span>

<span data-ttu-id="3de7a-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3de7a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3de7a-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3de7a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de7a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3de7a-107">Syntax</span></span>

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="3de7a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3de7a-108">Members</span></span>

<span data-ttu-id="3de7a-109">A classe **\_ \_ InstanceDeletionEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3de7a-109">The **\_\_InstanceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="3de7a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3de7a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3de7a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3de7a-111">Properties</span></span>

<span data-ttu-id="3de7a-112">A classe **\_ \_ InstanceDeletionEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3de7a-112">The **\_\_InstanceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3de7a-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="3de7a-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3de7a-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="3de7a-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3de7a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3de7a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3de7a-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="3de7a-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="3de7a-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="3de7a-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="3de7a-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="3de7a-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3de7a-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="3de7a-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3de7a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3de7a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3de7a-121">Cópia da instância que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="3de7a-121">Copy of the instance that was deleted.</span></span> <span data-ttu-id="3de7a-122">Essa propriedade é herdada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="3de7a-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3de7a-123">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="3de7a-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3de7a-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3de7a-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3de7a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3de7a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3de7a-126">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="3de7a-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="3de7a-127">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="3de7a-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="3de7a-128">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="3de7a-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="3de7a-129">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="3de7a-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="3de7a-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3de7a-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3de7a-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="3de7a-131">Remarks</span></span>

<span data-ttu-id="3de7a-132">A classe **\_ \_ InstanceDeletionEvent** é derivada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="3de7a-132">The **\_\_InstanceDeletionEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="3de7a-133">**Exclusão de um recurso: \_ \_ InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="3de7a-133">**Deletion of a resource: \_\_InstanceDeletionEvent**</span></span>

<span data-ttu-id="3de7a-134">Se você quiser garantir que um programa de verificação antivírus específico continue a ser executado em um computador, você pode gravar um script que monitora os processos no computador para determinar se algum deles parou.</span><span class="sxs-lookup"><span data-stu-id="3de7a-134">If you want to ensure that a particular antivirus scanner program continues to run on a computer, you can write a script that monitors the processes on the computer to determine whether any of them stop.</span></span>

<span data-ttu-id="3de7a-135">As consultas de notificação que solicitam a notificação da exclusão de um recurso e usam eventos intrínsecos usam uma sintaxe semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="3de7a-135">Notification queries that request notification of the deletion of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a><span data-ttu-id="3de7a-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3de7a-136">Examples</span></span>

<span data-ttu-id="3de7a-137">O exemplo de código VBScript do [evento monitor processo de exclusão de processos](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) na galeria do TechNet usa **\_ \_ InstanceDeletionEvent** para monitorar a primeira ocorrência de um evento de exclusão de instância do WMI para o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="3de7a-137">The [Monitor process deletion event](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript code sample on TechNet Gallery uses **\_\_InstanceDeletionEvent** to monitor the first occurrence of a WMI instance deletion event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="3de7a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3de7a-138">Requirements</span></span>



| <span data-ttu-id="3de7a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="3de7a-139">Requirement</span></span> | <span data-ttu-id="3de7a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="3de7a-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3de7a-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3de7a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3de7a-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3de7a-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3de7a-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3de7a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3de7a-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3de7a-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3de7a-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="3de7a-145">Namespace</span></span><br/>                | <span data-ttu-id="3de7a-146">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="3de7a-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3de7a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="3de7a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de7a-148">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="3de7a-148">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="3de7a-149">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="3de7a-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

