---
description: Essa classe é a classe pai para eventos de e/s de divisão. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: Classe SplitIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967723"
---
# <a name="splitio-class"></a><span data-ttu-id="53112-104">Classe SplitIo</span><span class="sxs-lookup"><span data-stu-id="53112-104">SplitIo class</span></span>

<span data-ttu-id="53112-105">Essa classe é a classe pai para eventos de e/s de divisão.</span><span class="sxs-lookup"><span data-stu-id="53112-105">This class is the parent class for split IO events.</span></span>

<span data-ttu-id="53112-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="53112-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="53112-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53112-107">Syntax</span></span>

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="53112-108">Membros</span><span class="sxs-lookup"><span data-stu-id="53112-108">Members</span></span>

<span data-ttu-id="53112-109">A classe **SplitIo** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="53112-109">The **SplitIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="53112-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="53112-110">Remarks</span></span>

<span data-ttu-id="53112-111">Para habilitar eventos de e/s de divisão em uma sessão de log de kernel NT, especifique o sinalizador de **\_ \_ \_ \_ e/s de divisão do sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="53112-111">To enable split IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_SPLIT\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="53112-112">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de e/s de divisão chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**SplitIoGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="53112-112">Event trace consumers can implement special processing for split IO events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**SplitIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="53112-113">Use o seguinte tipo de evento para identificar o evento real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="53112-113">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="53112-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="53112-114">Event type</span></span>           | <span data-ttu-id="53112-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="53112-115">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53112-116">Valor do tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="53112-116">Event type value, 32</span></span> | <span data-ttu-id="53112-117">Dividir evento de e/s.</span><span class="sxs-lookup"><span data-stu-id="53112-117">Split IO event.</span></span> <span data-ttu-id="53112-118">A classe MOF [**SplitIo \_ info**](splitio-info.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="53112-118">The [**SplitIo\_Info**](splitio-info.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="53112-119">Eventos de e/s de divisão indicam que as solicitações de e/s foram divididas em várias solicitações de e/s de disco devido ao hardware de disco de espelhamento subjacente.</span><span class="sxs-lookup"><span data-stu-id="53112-119">Split IO events indicate that the IO requests have been split into multiple disk IO requests due to the underlying mirroring disk hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="53112-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53112-120">Requirements</span></span>



| <span data-ttu-id="53112-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="53112-121">Requirement</span></span> | <span data-ttu-id="53112-122">Valor</span><span class="sxs-lookup"><span data-stu-id="53112-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53112-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53112-123">Minimum supported client</span></span><br/> | <span data-ttu-id="53112-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53112-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53112-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53112-125">Minimum supported server</span></span><br/> | <span data-ttu-id="53112-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53112-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
