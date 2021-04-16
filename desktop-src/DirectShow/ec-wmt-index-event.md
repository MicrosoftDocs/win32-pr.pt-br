---
description: Enviado quando um aplicativo usa o filtro de gravador ASF do WM para indexar arquivos de vídeo do Windows Media.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782248"
---
# <a name="ec_wmt_index_event-dshowh"></a><span data-ttu-id="ff53c-103">EC_WMT_INDEX_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="ff53c-103">EC_WMT_INDEX_EVENT (Dshow.h)</span></span>

<span data-ttu-id="ff53c-104">Enviado quando um aplicativo usa o filtro de [gravador ASF do WM](wm-asf-writer-filter.md) para indexar arquivos de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ff53c-104">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) filter to index Windows Media Video files.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff53c-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff53c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff53c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ff53c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ff53c-107">Pode ser uma das seguintes mensagens **de \_ status WMT** .</span><span class="sxs-lookup"><span data-stu-id="ff53c-107">Can be one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="ff53c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ff53c-108">Value</span></span>                | <span data-ttu-id="ff53c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff53c-109">Description</span></span>              |
|----------------------|--------------------------|
| <span data-ttu-id="ff53c-110">WMT \_ iniciado</span><span class="sxs-lookup"><span data-stu-id="ff53c-110">WMT\_STARTED</span></span>         | <span data-ttu-id="ff53c-111">A indexação foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="ff53c-111">Indexing has begun.</span></span>      |
| <span data-ttu-id="ff53c-112">WMT \_ fechado</span><span class="sxs-lookup"><span data-stu-id="ff53c-112">WMT\_CLOSED</span></span>          | <span data-ttu-id="ff53c-113">A indexação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="ff53c-113">Indexing has completed.</span></span>  |
| <span data-ttu-id="ff53c-114">\_progresso do índice de WMT \_</span><span class="sxs-lookup"><span data-stu-id="ff53c-114">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="ff53c-115">A indexação está em andamento.</span><span class="sxs-lookup"><span data-stu-id="ff53c-115">Indexing is in progress.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ff53c-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ff53c-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ff53c-117">Se *lParam1* for WMT \_ Closed ou WMT \_ iniciado, *lParam2* será zero.</span><span class="sxs-lookup"><span data-stu-id="ff53c-117">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="ff53c-118">Se *lParam1* for WMT \_ index \_ Progress, *lParam2* será um **DWORD** que especifica o andamento atual como uma porcentagem do tamanho total do download.</span><span class="sxs-lookup"><span data-stu-id="ff53c-118">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that specifies the current progress as a percentage of the total download size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff53c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff53c-119">Requirements</span></span>



| <span data-ttu-id="ff53c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff53c-120">Requirement</span></span> | <span data-ttu-id="ff53c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ff53c-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff53c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff53c-122">Header</span></span><br/> | <dl> <span data-ttu-id="ff53c-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff53c-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff53c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff53c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff53c-125">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="ff53c-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ff53c-126">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="ff53c-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




