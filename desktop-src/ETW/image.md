---
description: Essa classe é a classe pai para eventos de imagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Classe Image
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967980"
---
# <a name="image-class"></a><span data-ttu-id="af01e-104">Classe Image</span><span class="sxs-lookup"><span data-stu-id="af01e-104">Image class</span></span>

<span data-ttu-id="af01e-105">Essa classe é a classe pai para eventos de imagem.</span><span class="sxs-lookup"><span data-stu-id="af01e-105">This class is the parent class for image events.</span></span>

<span data-ttu-id="af01e-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="af01e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="af01e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af01e-107">Syntax</span></span>

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="af01e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="af01e-108">Members</span></span>

<span data-ttu-id="af01e-109">A classe **Image** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="af01e-109">The **Image** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="af01e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="af01e-110">Remarks</span></span>

<span data-ttu-id="af01e-111">Para habilitar eventos de imagem em uma sessão de log de kernel NT, especifique o sinalizador de carregamento de imagem do sinalizador de rastreamento de eventos no membro **EnableFlags** da estrutura [](/windows/win32/api/evntrace/nf-evntrace-starttracea) de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função StartTrace. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af01e-111">To enable image events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_IMAGE\_LOAD** flag in the **EnableFlags** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="af01e-112">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de carregamento de imagem chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ImageLoadGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="af01e-112">Event trace consumers can implement special processing for image load events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ImageLoadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="af01e-113">Use os seguintes tipos de evento para identificar eventos de carga de imagem ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="af01e-113">Use the following event types to identify image load events when consuming events.</span></span>



| <span data-ttu-id="af01e-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="af01e-114">Event type</span></span>                                                          | <span data-ttu-id="af01e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="af01e-115">Description</span></span>                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af01e-116">**Evento \_ de \_ \_ Carga de tipo de rastreamento**(o valor do tipo de evento é 10)</span><span class="sxs-lookup"><span data-stu-id="af01e-116">**EVENT\_TRACE\_TYPE\_LOAD**(Event type value is 10)</span></span><br/>     | <span data-ttu-id="af01e-117">Evento de carregamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="af01e-117">Image load event.</span></span> <span data-ttu-id="af01e-118">Gerado quando um arquivo DLL ou executável é carregado.</span><span class="sxs-lookup"><span data-stu-id="af01e-118">Generated when a DLL or executable file is loaded.</span></span> <span data-ttu-id="af01e-119">O provedor gera apenas um evento pela primeira vez que uma determinada DLL é carregada.</span><span class="sxs-lookup"><span data-stu-id="af01e-119">The provider generates only one event for the first time a given DLL is loaded.</span></span> <span data-ttu-id="af01e-120">A classe MOF de [**\_ carregamento de imagem**](image-load.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="af01e-120">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="af01e-121">**Evento \_ de Tipo de rastreamento \_ \_ end**(o valor do tipo de evento é 2)</span><span class="sxs-lookup"><span data-stu-id="af01e-121">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>       | <span data-ttu-id="af01e-122">Evento de descarregamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="af01e-122">Image unload event.</span></span> <span data-ttu-id="af01e-123">Gerado quando um arquivo DLL ou executável é descarregado.</span><span class="sxs-lookup"><span data-stu-id="af01e-123">Generated when a DLL or executable file is unloaded.</span></span> <span data-ttu-id="af01e-124">O provedor gera apenas um evento para a última vez em que uma determinada DLL é descarregada.</span><span class="sxs-lookup"><span data-stu-id="af01e-124">The provider generates only one event for the last time a given DLL is unloaded.</span></span> <span data-ttu-id="af01e-125">A classe MOF de [**\_ carregamento de imagem**](image-load.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="af01e-125">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="af01e-126">**Evento \_ de Tipo de rastreamento \_ \_ DC \_ Iniciar**(o valor do tipo de evento é 3)</span><span class="sxs-lookup"><span data-stu-id="af01e-126">**EVENT\_TRACE\_TYPE\_DC\_START**(Event type value is 3)</span></span><br/> | <span data-ttu-id="af01e-127">Evento de início de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="af01e-127">Data collection start event.</span></span> <span data-ttu-id="af01e-128">Enumera todas as imagens carregadas no início do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="af01e-128">Enumerates all loaded images at the beginning of the trace.</span></span> <span data-ttu-id="af01e-129">A classe MOF de [**\_ carregamento de imagem**](image-load.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="af01e-129">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="af01e-130">**Evento \_ de Tipo de rastreamento \_ \_ DC \_ end**(o valor do tipo de evento é 4)</span><span class="sxs-lookup"><span data-stu-id="af01e-130">**EVENT\_TRACE\_TYPE\_DC\_END**(Event type value is 4)</span></span><br/>   | <span data-ttu-id="af01e-131">Evento de término da coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="af01e-131">Data collection end event.</span></span> <span data-ttu-id="af01e-132">Enumera todas as imagens carregadas no final do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="af01e-132">Enumerates all loaded images at the end of the trace.</span></span> <span data-ttu-id="af01e-133">A classe MOF de [**\_ carregamento de imagem**](image-load.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="af01e-133">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="af01e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af01e-134">Requirements</span></span>



| <span data-ttu-id="af01e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="af01e-135">Requirement</span></span> | <span data-ttu-id="af01e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="af01e-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af01e-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af01e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="af01e-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af01e-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af01e-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af01e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="af01e-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af01e-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af01e-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="af01e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af01e-142">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="af01e-142">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="af01e-143">**Carregamento de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="af01e-143">**Image\_Load**</span></span>](image-load.md)
</dt> <dt>

[<span data-ttu-id="af01e-144">**V0 de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="af01e-144">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="af01e-145">**Imagem \_ v1**</span><span class="sxs-lookup"><span data-stu-id="af01e-145">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 
