---
description: A classe pai para eventos de cabeçalho de log. Essa classe é sempre a primeira classe de rastreamento de eventos enviada a um consumidor (esse evento não é enviado para consumidores em tempo real). A sintaxe a seguir é simplificada do código MOF.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: Classe EventTraceEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967430"
---
# <a name="eventtraceevent-class"></a><span data-ttu-id="9221f-105">Classe EventTraceEvent</span><span class="sxs-lookup"><span data-stu-id="9221f-105">EventTraceEvent class</span></span>

<span data-ttu-id="9221f-106">A classe pai para eventos de cabeçalho de log.</span><span class="sxs-lookup"><span data-stu-id="9221f-106">The parent class for log header events.</span></span> <span data-ttu-id="9221f-107">Essa classe é sempre a primeira classe de rastreamento de eventos enviada a um consumidor (esse evento não é enviado para consumidores em tempo real).</span><span class="sxs-lookup"><span data-stu-id="9221f-107">This class is always the first event trace class sent to a consumer (this event is not sent to real-time consumers).</span></span>

<span data-ttu-id="9221f-108">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="9221f-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9221f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9221f-109">Syntax</span></span>

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="9221f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="9221f-110">Members</span></span>

<span data-ttu-id="9221f-111">A classe **EventTraceEvent** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="9221f-111">The **EventTraceEvent** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="9221f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9221f-112">Requirements</span></span>



| <span data-ttu-id="9221f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9221f-113">Requirement</span></span> | <span data-ttu-id="9221f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9221f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9221f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9221f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9221f-116">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9221f-116">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9221f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9221f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9221f-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9221f-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9221f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9221f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9221f-120">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="9221f-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="9221f-121">**\_Cabeçalho EventTrace**</span><span class="sxs-lookup"><span data-stu-id="9221f-121">**EventTrace\_Header**</span></span>](eventtrace-header.md)
</dt> </dl>

 

 




