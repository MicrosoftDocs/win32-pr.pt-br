---
description: Essa classe é a classe pai para eventos de rastreamento de pilha.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: Classe StackWalk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967418"
---
# <a name="stackwalk-class"></a><span data-ttu-id="48f96-103">Classe StackWalk</span><span class="sxs-lookup"><span data-stu-id="48f96-103">StackWalk class</span></span>

<span data-ttu-id="48f96-104">Essa classe é a classe pai para eventos de rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="48f96-104">This class is the parent class for stack tracing events.</span></span>

<span data-ttu-id="48f96-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="48f96-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f96-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48f96-106">Syntax</span></span>

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="48f96-107">Membros</span><span class="sxs-lookup"><span data-stu-id="48f96-107">Members</span></span>

<span data-ttu-id="48f96-108">A classe **StackWalk** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="48f96-108">The **StackWalk** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="48f96-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="48f96-109">Remarks</span></span>

<span data-ttu-id="48f96-110">Para habilitar o rastreamento de pilha de eventos de kernel, chame a função [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) e especifique os eventos de kernel e os tipos para os quais você deseja capturar o rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="48f96-110">To enable stack tracing of kernel events, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function and specify the kernel events and types for which you want to capture the stack trace.</span></span> <span data-ttu-id="48f96-111">Para habilitar o rastreamento de pilha para outros eventos, defina o membro **preaptoproperty** de [**habilitar \_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) para **evento \_ habilitar \_ rastreamento de \_ pilha \_ de propriedades**.</span><span class="sxs-lookup"><span data-stu-id="48f96-111">To enable stack tracing for other events, set the **EnableProperty** member of [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) to **EVENT\_ENABLE\_PROPERTY\_STACK\_TRACE**.</span></span>

<span data-ttu-id="48f96-112">Use o seguinte tipo de evento para identificar o evento real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="48f96-112">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="48f96-113">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="48f96-113">Event type</span></span>           | <span data-ttu-id="48f96-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="48f96-114">Description</span></span>                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f96-115">Valor do tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="48f96-115">Event type value, 32</span></span> | <span data-ttu-id="48f96-116">Evento de rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="48f96-116">Stack tracing event.</span></span> <span data-ttu-id="48f96-117">A classe MOF do [**\_ evento StackWalk**](stackwalk-event.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="48f96-117">The [**StackWalk\_Event**](stackwalk-event.md) MOF class defines the event data for this event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="48f96-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48f96-118">Requirements</span></span>



| <span data-ttu-id="48f96-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="48f96-119">Requirement</span></span> | <span data-ttu-id="48f96-120">Valor</span><span class="sxs-lookup"><span data-stu-id="48f96-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="48f96-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48f96-121">Minimum supported client</span></span><br/> | <span data-ttu-id="48f96-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="48f96-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="48f96-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48f96-123">Minimum supported server</span></span><br/> | <span data-ttu-id="48f96-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="48f96-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 
