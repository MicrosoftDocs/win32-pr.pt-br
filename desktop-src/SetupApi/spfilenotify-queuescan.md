---
description: A \_ notificação SPFILENOTIFY QUEUESCAN é enviada a uma rotina de retorno de chamada por SetupScanFileQueue para cada nó na subfila de cópia da fila de arquivos. Isso só ocorrerá se a função SetupScanFileQueue tiver sido chamada especificando o sinalizador SPQ da \_ verificação \_ usar o retorno de \_ chamada.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: Mensagem de SPFILENOTIFY_QUEUESCAN (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755546"
---
# <a name="spfilenotify_queuescan-message"></a><span data-ttu-id="c2118-104">\_Mensagem SPFILENOTIFY QUEUESCAN</span><span class="sxs-lookup"><span data-stu-id="c2118-104">SPFILENOTIFY\_QUEUESCAN message</span></span>

<span data-ttu-id="c2118-105">A notificação **SPFILENOTIFY \_ QUEUESCAN** é enviada a uma rotina de retorno de chamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nó na subfila de cópia da fila de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c2118-105">The **SPFILENOTIFY\_QUEUESCAN** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="c2118-106">Isso só ocorrerá se a função **SetupScanFileQueue** tiver sido chamada especificando o sinalizador SPQ da \_ verificação \_ usar o retorno de \_ chamada.</span><span class="sxs-lookup"><span data-stu-id="c2118-106">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a><span data-ttu-id="c2118-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2118-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2118-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="c2118-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="c2118-109">Cadeia de caracteres terminada em nulo que especifica as informações de caminho de destino para o arquivo na fila no nó atual.</span><span class="sxs-lookup"><span data-stu-id="c2118-109">Null-terminated string that specifies the target path information for the file queued in the current node.</span></span>

</dd> <dt>

<span data-ttu-id="c2118-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="c2118-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="c2118-111">Se o arquivo no nó atual da fila estiver em uso, *param2* usará a cópia atrasada do valor SPQ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c2118-111">If the file in the current node of the queue is in use, *Param2* takes the value SPQ\_DELAYED\_COPY.</span></span> <span data-ttu-id="c2118-112">Se o arquivo não estiver em uso, o valor será zero.</span><span class="sxs-lookup"><span data-stu-id="c2118-112">If the file is not in use, the value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2118-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2118-113">Return value</span></span>

<span data-ttu-id="c2118-114">A rotina de retorno de chamada deve retornar um [código de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c2118-114">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="c2118-115">Se a rotina de retorno de chamada não retornar nenhum \_ erro, a verificação da fila continuará.</span><span class="sxs-lookup"><span data-stu-id="c2118-115">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="c2118-116">Se a rotina retornar qualquer outro código de erro, a verificação de fila aborta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retorna **false**.</span><span class="sxs-lookup"><span data-stu-id="c2118-116">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="c2118-117">Essa notificação não é tratada pela função [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="c2118-117">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2118-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2118-118">Requirements</span></span>



| <span data-ttu-id="c2118-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2118-119">Requirement</span></span> | <span data-ttu-id="c2118-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c2118-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2118-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2118-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2118-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c2118-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c2118-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2118-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2118-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2118-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2118-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2118-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2118-126"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2118-126"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2118-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2118-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2118-128">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c2118-128">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="c2118-129">Notificações</span><span class="sxs-lookup"><span data-stu-id="c2118-129">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="c2118-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="c2118-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

