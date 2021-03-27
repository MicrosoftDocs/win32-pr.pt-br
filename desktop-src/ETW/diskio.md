---
description: Essa classe é a classe pai para eventos de e/s de disco. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: Classe DiskIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920736"
---
# <a name="diskio-class"></a><span data-ttu-id="102ec-104">Classe DiskIo</span><span class="sxs-lookup"><span data-stu-id="102ec-104">DiskIo class</span></span>

<span data-ttu-id="102ec-105">Essa classe é a classe pai para eventos de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="102ec-105">This class is the parent class for disk I/O events.</span></span>

<span data-ttu-id="102ec-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="102ec-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="102ec-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="102ec-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="102ec-108">Membros</span><span class="sxs-lookup"><span data-stu-id="102ec-108">Members</span></span>

<span data-ttu-id="102ec-109">A classe **DiskIo** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="102ec-109">The **DiskIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="102ec-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="102ec-110">Remarks</span></span>

<span data-ttu-id="102ec-111">Para habilitar eventos I/0 de disco em uma sessão de log de kernel NT, especifique o sinalizador de **\_ \_ \_ \_ e/s do disco do sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="102ec-111">To enable disk I/0 events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="102ec-112">Você também pode especificar um ou mais dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="102ec-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="102ec-113">**sinalizador de rastreamento de eventos \_ \_ \_ inicialização de \_ e/s de disco \_**</span><span class="sxs-lookup"><span data-stu-id="102ec-113">**EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT**</span></span>
-   <span data-ttu-id="102ec-114">**\_Driver de \_ sinalizador de rastreamento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="102ec-114">**EVENT\_TRACE\_FLAG\_DRIVER**</span></span>

<span data-ttu-id="102ec-115">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de e/s de disco chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**DiskIoGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="102ec-115">Event trace consumers can implement special processing for disk I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**DiskIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="102ec-116">Use os seguintes tipos de evento para identificar o evento de e/s de disco real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="102ec-116">Use the following event types to identify the actual disk I/O event when consuming events.</span></span>



| <span data-ttu-id="102ec-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="102ec-117">Event type</span></span>                                                                      | <span data-ttu-id="102ec-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="102ec-118">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102ec-119">**Evento \_ de \_Leitura de \_ e \_ /s do tipo de rastreamento**(o valor do tipo de evento é 10)</span><span class="sxs-lookup"><span data-stu-id="102ec-119">**EVENT\_TRACE\_TYPE\_IO\_READ**(Event type value is 10)</span></span><br/>             | <span data-ttu-id="102ec-120">Ler evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-120">Read event.</span></span> <span data-ttu-id="102ec-121">A classe [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-121">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                              |
| <span data-ttu-id="102ec-122">**Evento \_ de \_Gravação de \_ e \_ /s do tipo de rastreamento**(o valor do tipo de evento é 11)</span><span class="sxs-lookup"><span data-stu-id="102ec-122">**EVENT\_TRACE\_TYPE\_IO\_WRITE**(Event type value is 11)</span></span><br/>            | <span data-ttu-id="102ec-123">Evento de gravação.</span><span class="sxs-lookup"><span data-stu-id="102ec-123">Write event.</span></span> <span data-ttu-id="102ec-124">A classe [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-124">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                             |
| <span data-ttu-id="102ec-125">**Evento \_ de Tipo de rastreamento \_ \_ e/s \_ leitura \_ init**(o valor do tipo de evento é 12)</span><span class="sxs-lookup"><span data-stu-id="102ec-125">**EVENT\_TRACE\_TYPE\_IO\_READ\_INIT**(Event type value is 12)</span></span><br/>       | <span data-ttu-id="102ec-126">Inicializar evento de leitura.</span><span class="sxs-lookup"><span data-stu-id="102ec-126">Initialize read event.</span></span> <span data-ttu-id="102ec-127">A classe [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-127">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="102ec-128">**Evento \_ de Tipo de rastreamento \_ \_ Io \_ Write \_ init**(o valor do tipo de evento é 13)</span><span class="sxs-lookup"><span data-stu-id="102ec-128">**EVENT\_TRACE\_TYPE\_IO\_WRITE\_INIT**(Event type value is 13)</span></span><br/>      | <span data-ttu-id="102ec-129">Inicializar evento de gravação.</span><span class="sxs-lookup"><span data-stu-id="102ec-129">Initialize write event.</span></span> <span data-ttu-id="102ec-130">A classe [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-130">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="102ec-131">**Evento \_ de Tipo de rastreamento \_ \_ e \_ liberação de e/s**(o valor do tipo de evento é 14)</span><span class="sxs-lookup"><span data-stu-id="102ec-131">**EVENT\_TRACE\_TYPE\_IO\_FLUSH**(Event type value is 14)</span></span><br/>            | <span data-ttu-id="102ec-132">Inicializar evento de gravação.</span><span class="sxs-lookup"><span data-stu-id="102ec-132">Initialize write event.</span></span> <span data-ttu-id="102ec-133">A classe [**DiskIo \_ TypeGroup3**](diskio-typegroup3.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-133">The [**DiskIo\_TypeGroup3**](diskio-typegroup3.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="102ec-134">**Evento \_ de Tipo de rastreamento \_ \_ Io \_ flush \_ init**(o valor do tipo de evento é 15)</span><span class="sxs-lookup"><span data-stu-id="102ec-134">**EVENT\_TRACE\_TYPE\_IO\_FLUSH\_INIT**(Event type value is 15)</span></span><br/>      | <span data-ttu-id="102ec-135">Inicializar evento de liberação.</span><span class="sxs-lookup"><span data-stu-id="102ec-135">Initialize flush event.</span></span> <span data-ttu-id="102ec-136">A classe [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-136">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="102ec-137">**Evento \_ de Tipo de rastreamento \_ \_ e/s \_ \_ inicialização redirecionada**(o valor do tipo de evento é 16)</span><span class="sxs-lookup"><span data-stu-id="102ec-137">**EVENT\_TRACE\_TYPE\_IO\_REDIRECTED\_INIT**(Event type value is 16)</span></span><br/> | <span data-ttu-id="102ec-138">Inicializar evento Redirecionado.</span><span class="sxs-lookup"><span data-stu-id="102ec-138">Initialize redirected event.</span></span> <span data-ttu-id="102ec-139">Os eventos de e/s redirecionados são usados para mapear o IOs de disco para um formato WIM (Windows Imaging) para o nome de arquivo dentro do WIM.</span><span class="sxs-lookup"><span data-stu-id="102ec-139">Redirected IO events are used to map disk IOs to a Windows Imaging Format (WIM) to the filename within the WIM.</span></span>                  |
| <span data-ttu-id="102ec-140">O valor do tipo de evento é 52</span><span class="sxs-lookup"><span data-stu-id="102ec-140">Event type value is 52</span></span><br/>                                               | <span data-ttu-id="102ec-141">Evento de solicitação de conclusão de driver.</span><span class="sxs-lookup"><span data-stu-id="102ec-141">Driver complete request event.</span></span> <span data-ttu-id="102ec-142">A classe MOF [**DriverCompleteRequest**](drivercompleterequest.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-142">The [**DriverCompleteRequest**](drivercompleterequest.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="102ec-143">O valor do tipo de evento é 53</span><span class="sxs-lookup"><span data-stu-id="102ec-143">Event type value is 53</span></span><br/>                                               | <span data-ttu-id="102ec-144">Evento de retorno de solicitação de conclusão de driver.</span><span class="sxs-lookup"><span data-stu-id="102ec-144">Driver complete request return event.</span></span> <span data-ttu-id="102ec-145">A classe MOF [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-145">The [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="102ec-146">O valor do tipo de evento é 37</span><span class="sxs-lookup"><span data-stu-id="102ec-146">Event type value is 37</span></span><br/>                                               | <span data-ttu-id="102ec-147">Evento de rotina de conclusão do driver.</span><span class="sxs-lookup"><span data-stu-id="102ec-147">Driver completion routine event.</span></span> <span data-ttu-id="102ec-148">A classe MOF [**DriverCompletionRoutine**](drivercompletionroutine.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-148">The [**DriverCompletionRoutine**](drivercompletionroutine.md) MOF class defines the event data for this event.</span></span>              |
| <span data-ttu-id="102ec-149">O valor do tipo de evento é 34</span><span class="sxs-lookup"><span data-stu-id="102ec-149">Event type value is 34</span></span><br/>                                               | <span data-ttu-id="102ec-150">Evento de chamada de função principal do driver.</span><span class="sxs-lookup"><span data-stu-id="102ec-150">Driver major function call event.</span></span> <span data-ttu-id="102ec-151">A classe MOF [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-151">The [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) MOF class defines the event data for this event.</span></span>             |
| <span data-ttu-id="102ec-152">O valor do tipo de evento é 35</span><span class="sxs-lookup"><span data-stu-id="102ec-152">Event type value is 35</span></span><br/>                                               | <span data-ttu-id="102ec-153">Evento de retorno de chamada de função principal do driver.</span><span class="sxs-lookup"><span data-stu-id="102ec-153">Driver major function call return event.</span></span> <span data-ttu-id="102ec-154">A classe MOF [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="102ec-154">The [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="102ec-155">O provedor I/0 de disco não pode identificar qual arquivo é lido ou gravado durante um evento de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="102ec-155">The disk I/0 provider cannot identify which file is read or written during a disk I/O event.</span></span> <span data-ttu-id="102ec-156">Para recuperar o nome do arquivo associado ao evento de e/s de disco, habilite o provedor de eventos arquivo I/0.</span><span class="sxs-lookup"><span data-stu-id="102ec-156">To retrieve the name of the file associated with the disk I/O event, enable the file I/0 event provider.</span></span>

<span data-ttu-id="102ec-157">Os eventos de e/s de disco são registrados no tempo de conclusão de e/s.</span><span class="sxs-lookup"><span data-stu-id="102ec-157">Disk I/O events are recorded at the I/O completion time.</span></span> <span data-ttu-id="102ec-158">Para determinar quando a operação de e/s foi iniciada, use os eventos de inicialização, por exemplo, o tipo de rastreamento de evento \_ \_ \_ Io \_ Read \_ init.</span><span class="sxs-lookup"><span data-stu-id="102ec-158">To determine when the I/O operation began, use the initialization events, for example, EVENT\_TRACE\_TYPE\_IO\_READ\_INIT.</span></span>

## <a name="requirements"></a><span data-ttu-id="102ec-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="102ec-159">Requirements</span></span>



| <span data-ttu-id="102ec-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="102ec-160">Requirement</span></span> | <span data-ttu-id="102ec-161">Valor</span><span class="sxs-lookup"><span data-stu-id="102ec-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="102ec-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="102ec-162">Minimum supported client</span></span><br/> | <span data-ttu-id="102ec-163">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="102ec-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="102ec-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="102ec-164">Minimum supported server</span></span><br/> | <span data-ttu-id="102ec-165">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="102ec-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="102ec-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="102ec-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102ec-167">**DiskIo \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="102ec-167">**DiskIo\_TypeGroup1**</span></span>](diskio-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="102ec-168">**DiskIo \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="102ec-168">**DiskIo\_TypeGroup2**</span></span>](diskio-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="102ec-169">**DiskIo \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="102ec-169">**DiskIo\_TypeGroup3**</span></span>](diskio-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="102ec-170">**DriverCompleteRequest**</span><span class="sxs-lookup"><span data-stu-id="102ec-170">**DriverCompleteRequest**</span></span>](drivercompleterequest.md)
</dt> <dt>

[<span data-ttu-id="102ec-171">**DriverCompleteRequestReturn**</span><span class="sxs-lookup"><span data-stu-id="102ec-171">**DriverCompleteRequestReturn**</span></span>](drivercompleterequestreturn.md)
</dt> <dt>

[<span data-ttu-id="102ec-172">**DriverCompletionRoutine**</span><span class="sxs-lookup"><span data-stu-id="102ec-172">**DriverCompletionRoutine**</span></span>](drivercompletionroutine.md)
</dt> <dt>

[<span data-ttu-id="102ec-173">**DriverMajorFunctionCall**</span><span class="sxs-lookup"><span data-stu-id="102ec-173">**DriverMajorFunctionCall**</span></span>](drivermajorfunctioncall.md)
</dt> <dt>

[<span data-ttu-id="102ec-174">**DriverMajorFunctionReturn**</span><span class="sxs-lookup"><span data-stu-id="102ec-174">**DriverMajorFunctionReturn**</span></span>](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
