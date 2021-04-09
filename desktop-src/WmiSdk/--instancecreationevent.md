---
description: Relata um evento de criação de instância, que é um tipo de evento intrínseco que é gerado quando uma nova instância é adicionada ao namespace.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: Classe __InstanceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171463"
---
# <a name="__instancecreationevent-class"></a><span data-ttu-id="8dfc0-103">\_\_Classe InstanceCreationEvent</span><span class="sxs-lookup"><span data-stu-id="8dfc0-103">\_\_InstanceCreationEvent class</span></span>

<span data-ttu-id="8dfc0-104">A classe de sistema **\_ \_ InstanceCreationEvent** relata um evento de criação de instância, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que é gerado quando uma nova instância é adicionada ao namespace.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-104">The **\_\_InstanceCreationEvent** system class reports an instance creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a new instance is added to the namespace.</span></span>

<span data-ttu-id="8dfc0-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8dfc0-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfc0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dfc0-107">Syntax</span></span>

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="8dfc0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8dfc0-108">Members</span></span>

<span data-ttu-id="8dfc0-109">A classe **\_ \_ InstanceCreationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8dfc0-109">The **\_\_InstanceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="8dfc0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8dfc0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8dfc0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8dfc0-111">Properties</span></span>

<span data-ttu-id="8dfc0-112">A classe **\_ \_ InstanceCreationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-112">The **\_\_InstanceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8dfc0-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfc0-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8dfc0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8dfc0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dfc0-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="8dfc0-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8dfc0-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dfc0-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfc0-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8dfc0-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8dfc0-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dfc0-121">Cópia da instância que foi criada.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-121">Copy of the instance that was created.</span></span> <span data-ttu-id="8dfc0-122">Essa propriedade é herdada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="8dfc0-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dfc0-123">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfc0-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8dfc0-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8dfc0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dfc0-126">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="8dfc0-127">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="8dfc0-128">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="8dfc0-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="8dfc0-129">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8dfc0-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="8dfc0-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8dfc0-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8dfc0-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="8dfc0-131">Remarks</span></span>

<span data-ttu-id="8dfc0-132">A classe **\_ \_ InstanceCreationEvent** é derivada de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="8dfc0-132">The **\_\_InstanceCreationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="8dfc0-133">**Criação de um recurso: \_ \_ InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-133">**Creation of a resource: \_\_InstanceCreationEvent**</span></span>

<span data-ttu-id="8dfc0-134">Suponha que você esteja interessado em receber uma notificação se o bloco de notas for executado em um determinado computador.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-134">Suppose you are interested in receiving a notification if Notepad is run on a certain computer.</span></span> <span data-ttu-id="8dfc0-135">Quando o bloco de notas é executado, um processo correspondente é criado.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-135">When Notepad runs, a corresponding process is created.</span></span> <span data-ttu-id="8dfc0-136">Os processos podem ser gerenciados usando o WMI e são representados pela classe de processo do Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="8dfc0-136">Processes can be managed by using WMI and are represented by the Win32\_Process class.</span></span> <span data-ttu-id="8dfc0-137">Quando o bloco de notas começa a ser executado, uma instância correspondente da \_ classe de processo Win32 fica disponível por meio do WMI.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-137">When Notepad starts running, a corresponding instance of the Win32\_Process class becomes available through WMI.</span></span> <span data-ttu-id="8dfc0-138">Se você registrou seu interesse nesse evento (emitindo a consulta de notificação de evento apropriada), a disponibilidade dessa instância resultará na criação de uma instância da classe **\_ \_ InstanceCreationEvent** .</span><span class="sxs-lookup"><span data-stu-id="8dfc0-138">If you have registered your interest in this event (by issuing the appropriate event notification query), the availability of this instance results in the creation of an instance of the **\_\_InstanceCreationEvent** class.</span></span>

<span data-ttu-id="8dfc0-139">As consultas de notificação que solicitam a notificação da criação de um recurso e usam eventos intrínsecos usam uma sintaxe semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="8dfc0-139">Notification queries that request notification of the creation of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

<span data-ttu-id="8dfc0-140">Para obter uma discussão maior sobre como usar o **\_ \_ InstanceCreationEvent** como uma maneira de monitorar sistemas de arquivos, consulte [WMI e monitoramento do sistema de arquivos](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) no CodeProject.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-140">For a larger discussion of using **\_\_InstanceCreationEvent** as a way to monitor file systems, see [WMI and File System Monitoring](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) on CodeProject.</span></span>

## <a name="examples"></a><span data-ttu-id="8dfc0-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8dfc0-141">Examples</span></span>

<span data-ttu-id="8dfc0-142">O exemplo de [criar registro de evento WMI permanente para monitorar arquivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) no PowerShell na galeria do TechNet usa **\_ \_ InstanceCreationEvent** como parte de um script complexo para configurar um registro de evento do WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-142">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a complex script to set up a permanent WMI event registration.</span></span>

<span data-ttu-id="8dfc0-143">O exemplo do PowerShell de [eventos permanentes do WMI](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) do PowerShell na galeria do TechNet usa **\_ \_ InstanceCreationEvent** como parte de um script de demonstração para configurar um registro de evento permanente.</span><span class="sxs-lookup"><span data-stu-id="8dfc0-143">The [PowerShell WMI Permanent Events](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a demonstration script for setting up a permanent event registration.</span></span>

<span data-ttu-id="8dfc0-144">O exemplo de teste de [evento de criação de processo](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) do VBScript no TechNet usa **\_ \_ InstanceCreationEvent** para monitorar o primeiro evento de criação de instância do WMI para o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="8dfc0-144">The [Monitor process creation event](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) VBScript sample on TechNet uses **\_\_InstanceCreationEvent** to monitors the first WMI instance creation event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="8dfc0-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dfc0-145">Requirements</span></span>



| <span data-ttu-id="8dfc0-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dfc0-146">Requirement</span></span> | <span data-ttu-id="8dfc0-147">Valor</span><span class="sxs-lookup"><span data-stu-id="8dfc0-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8dfc0-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dfc0-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8dfc0-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8dfc0-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8dfc0-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dfc0-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8dfc0-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dfc0-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8dfc0-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="8dfc0-152">Namespace</span></span><br/>                | <span data-ttu-id="8dfc0-153">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="8dfc0-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8dfc0-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="8dfc0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dfc0-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="8dfc0-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="8dfc0-156">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8dfc0-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

