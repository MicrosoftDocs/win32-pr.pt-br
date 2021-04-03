---
description: A \_ notificação endqueue do SPFILENOTIFY é enviada para a rotina de retorno de chamada quando todas as operações em fila foram concluídas.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: Mensagem de SPFILENOTIFY_ENDQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3ed2ca896f91ec09cb49f89731b41c5d099465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922728"
---
# <a name="spfilenotify_endqueue-message"></a><span data-ttu-id="e7493-103">Mensagem do SPFILENOTIFY \_ ENDqueue</span><span class="sxs-lookup"><span data-stu-id="e7493-103">SPFILENOTIFY\_ENDQUEUE message</span></span>

<span data-ttu-id="e7493-104">A **notificação \_ Endqueue do SPFILENOTIFY** é enviada para a rotina de retorno de chamada quando todas as operações em fila foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="e7493-104">The **SPFILENOTIFY\_ENDQUEUE** notification is sent to the callback routine when all of the queued operations have been completed.</span></span>


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="e7493-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7493-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7493-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="e7493-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="e7493-107">**True** se a fila tiver sido processada com êxito; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="e7493-107">**TRUE** if the queue was processed successfully, **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="e7493-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="e7493-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="e7493-109">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="e7493-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7493-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7493-110">Return value</span></span>

<span data-ttu-id="e7493-111">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="e7493-111">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7493-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7493-112">Requirements</span></span>



| <span data-ttu-id="e7493-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7493-113">Requirement</span></span> | <span data-ttu-id="e7493-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e7493-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7493-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7493-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e7493-116">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e7493-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e7493-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7493-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e7493-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7493-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7493-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7493-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7493-120"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7493-120"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7493-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7493-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7493-122">Visão geral</span><span class="sxs-lookup"><span data-stu-id="e7493-122">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="e7493-123">Notificações</span><span class="sxs-lookup"><span data-stu-id="e7493-123">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="e7493-124">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="e7493-124">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="e7493-125">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="e7493-125">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




