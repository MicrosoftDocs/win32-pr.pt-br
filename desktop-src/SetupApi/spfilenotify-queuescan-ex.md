---
description: A \_ notificação SPFILENOTIFY QUEUESCAN \_ ex é enviada para uma rotina de retorno de chamada por SetupScanFileQueue para cada nó na subfila de cópia da fila de arquivos.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Mensagem de SPFILENOTIFY_QUEUESCAN_EX (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827925"
---
# <a name="spfilenotify_queuescan_ex-message"></a><span data-ttu-id="cf1fd-103">\_Mensagem SPFILENOTIFY QUEUESCAN \_ ex</span><span class="sxs-lookup"><span data-stu-id="cf1fd-103">SPFILENOTIFY\_QUEUESCAN\_EX message</span></span>

<span data-ttu-id="cf1fd-104">A notificação **SPFILENOTIFY \_ QUEUESCAN \_ ex** é enviada para uma rotina de retorno de chamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nó na subfila de cópia da fila de arquivos.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-104">The **SPFILENOTIFY\_QUEUESCAN\_EX** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="cf1fd-105">Isso só ocorrerá se a função **SetupScanFileQueue** tiver sido chamada especificando o sinalizador SPQ de \_ verificação \_ usar \_ CALLBACKEX.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACKEX.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="cf1fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf1fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf1fd-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="cf1fd-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="cf1fd-108">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="cf1fd-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="cf1fd-109">O membro de **destino** é o nome do arquivo de destino no sistema.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-109">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="cf1fd-110">O membro de **origem** é o caminho esperado do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-110">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="cf1fd-111">O membro **Win32Error** é o erro de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-111">The **Win32Error** member is the signing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf1fd-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf1fd-112">Return value</span></span>

<span data-ttu-id="cf1fd-113">A rotina de retorno de chamada deve retornar um [código de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cf1fd-113">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="cf1fd-114">Se a rotina de retorno de chamada não retornar nenhum \_ erro, a verificação da fila continuará.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-114">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="cf1fd-115">Se a rotina retornar qualquer outro código de erro, a verificação de fila aborta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retorna false.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-115">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="cf1fd-116">Essa notificação não é tratada pela função [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="cf1fd-116">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf1fd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf1fd-117">Requirements</span></span>



| <span data-ttu-id="cf1fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf1fd-118">Requirement</span></span> | <span data-ttu-id="cf1fd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cf1fd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1fd-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf1fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cf1fd-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cf1fd-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cf1fd-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf1fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cf1fd-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf1fd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf1fd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf1fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf1fd-125"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf1fd-125"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf1fd-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf1fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf1fd-127">Visão geral</span><span class="sxs-lookup"><span data-stu-id="cf1fd-127">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="cf1fd-128">Notificações</span><span class="sxs-lookup"><span data-stu-id="cf1fd-128">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="cf1fd-129">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-129">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

