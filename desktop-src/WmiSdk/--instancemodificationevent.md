---
description: Relata um evento de modificação de instância, que é um tipo de evento intrínseco gerado quando uma instância é alterada no namespace.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: Classe __InstanceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829282"
---
# <a name="__instancemodificationevent-class"></a><span data-ttu-id="accb2-103">\_\_Classe InstanceModificationEvent</span><span class="sxs-lookup"><span data-stu-id="accb2-103">\_\_InstanceModificationEvent class</span></span>

<span data-ttu-id="accb2-104">A classe de sistema **\_ \_ InstanceModificationEvent** relata um evento de modificação de instância, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) gerado quando uma instância é alterada no namespace.</span><span class="sxs-lookup"><span data-stu-id="accb2-104">The **\_\_InstanceModificationEvent** system class reports an instance modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance changes in the namespace.</span></span>

<span data-ttu-id="accb2-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="accb2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="accb2-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="accb2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="accb2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="accb2-107">Syntax</span></span>

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="accb2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="accb2-108">Members</span></span>

<span data-ttu-id="accb2-109">A classe **\_ \_ InstanceModificationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="accb2-109">The **\_\_InstanceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="accb2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="accb2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="accb2-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="accb2-111">Properties</span></span>

<span data-ttu-id="accb2-112">A classe **\_ \_ InstanceModificationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="accb2-112">The **\_\_InstanceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="accb2-113">**PreviousInstance**</span><span class="sxs-lookup"><span data-stu-id="accb2-113">**PreviousInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="accb2-114">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="accb2-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="accb2-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="accb2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="accb2-116">Cópia da instância antes da modificação.</span><span class="sxs-lookup"><span data-stu-id="accb2-116">Copy of the instance prior to modification.</span></span>

</dd> <dt>

<span data-ttu-id="accb2-117">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="accb2-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="accb2-118">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="accb2-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="accb2-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="accb2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="accb2-120">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="accb2-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="accb2-121">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="accb2-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="accb2-122">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="accb2-122">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="accb2-123">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="accb2-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="accb2-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="accb2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="accb2-125">Nova versão da instância alterada.</span><span class="sxs-lookup"><span data-stu-id="accb2-125">New version of the changed instance.</span></span> <span data-ttu-id="accb2-126">Essa propriedade é herdada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="accb2-126">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="accb2-127">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="accb2-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="accb2-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="accb2-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="accb2-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="accb2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="accb2-130">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="accb2-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="accb2-131">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="accb2-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="accb2-132">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="accb2-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="accb2-133">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="accb2-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="accb2-134">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="accb2-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="accb2-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="accb2-135">Remarks</span></span>

<span data-ttu-id="accb2-136">A classe **\_ \_ InstanceModificationEvent** é derivada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="accb2-136">The **\_\_InstanceModificationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="accb2-137">**Modificação de um recurso: \_ \_ InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="accb2-137">**Modification of a resource: \_\_InstanceModificationEvent**</span></span>

<span data-ttu-id="accb2-138">Suponha que você suspeite que um aplicativo de gerenciamento que você está usando está alterando erroneamente o tipo de inicialização de um serviço em um de seus servidores.</span><span class="sxs-lookup"><span data-stu-id="accb2-138">Suppose you suspect that a management application you are using is erroneously changing the startup type of a service on one of your servers.</span></span> <span data-ttu-id="accb2-139">Você deseja escrever um script WMI para monitorar as modificações feitas na configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="accb2-139">You want to write a WMI script to monitor any modifications made to the configuration of the service.</span></span> <span data-ttu-id="accb2-140">Assim que uma modificação é feita em um serviço, seu TargetInstance correspondente reflete a modificação.</span><span class="sxs-lookup"><span data-stu-id="accb2-140">As soon as a modification is made to a service, its corresponding TargetInstance reflects the modification.</span></span>

<span data-ttu-id="accb2-141">Se você registrar seu interesse nesse evento, uma modificação na configuração do serviço resultará na criação de uma instância da classe **\_ \_ InstanceModificationEvent** .</span><span class="sxs-lookup"><span data-stu-id="accb2-141">If you register your interest in this event, a modification to the configuration of the service results in the creation of an instance of the **\_\_InstanceModificationEvent** class.</span></span>

<span data-ttu-id="accb2-142">As consultas de notificação que solicitam a notificação da modificação de um recurso e usam eventos intrínsecos usam uma sintaxe semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="accb2-142">Notification queries that request notification of the modification of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a><span data-ttu-id="accb2-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="accb2-143">Examples</span></span>

<span data-ttu-id="accb2-144">O exemplo de teste de [evento do monitor de modificação do processo](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) na galeria do TechNet usa **\_ \_ InstanceModificationEvent** para monitorar a primeira ocorrência de um evento de modificação da instância do WMI para o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="accb2-144">The [Monitor process modification event](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript sample on TechNet Gallery uses **\_\_InstanceModificationEvent** to monitor the first occurrence of a WMI instance modification event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="accb2-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="accb2-145">Requirements</span></span>



| <span data-ttu-id="accb2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="accb2-146">Requirement</span></span> | <span data-ttu-id="accb2-147">Valor</span><span class="sxs-lookup"><span data-stu-id="accb2-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="accb2-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="accb2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="accb2-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="accb2-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="accb2-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="accb2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="accb2-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="accb2-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="accb2-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="accb2-152">Namespace</span></span><br/>                | <span data-ttu-id="accb2-153">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="accb2-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="accb2-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="accb2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accb2-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="accb2-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="accb2-156">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="accb2-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

