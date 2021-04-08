---
title: EC_WMT_INDEX_EVENT (SDK do Windows Media Format 11)
description: evento de índice do EC \_ WMT \_ \_
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- SDK do Windows Media Format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- ASF (Advanced Systems Format), EC_WMT_INDEX_EVENT
- ASF (formato de sistemas avançados), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008695"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a><span data-ttu-id="5ff3f-108">EC_WMT_INDEX_EVENT (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="5ff3f-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="5ff3f-109">Enviado pelo Windows Media Format SDK quando um aplicativo usa o gravador ASF para indexar arquivos de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5ff3f-109">Sent by the Windows Media Format SDK when an application uses the ASF Writer to index Windows Media Video files.</span></span>

<span data-ttu-id="5ff3f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ff3f-110">Parameters</span></span>

<span data-ttu-id="5ff3f-111">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="5ff3f-111">*lParam1*</span></span>

<span data-ttu-id="5ff3f-112">Pode ser qualquer uma das seguintes mensagens **de \_ status WMT** .</span><span class="sxs-lookup"><span data-stu-id="5ff3f-112">Can be any one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="5ff3f-113">Mensagem</span><span class="sxs-lookup"><span data-stu-id="5ff3f-113">Message</span></span>              | <span data-ttu-id="5ff3f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ff3f-114">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="5ff3f-115">WMT \_ iniciado</span><span class="sxs-lookup"><span data-stu-id="5ff3f-115">WMT\_STARTED</span></span>         | <span data-ttu-id="5ff3f-116">A indexação foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="5ff3f-116">Indexing has begun.</span></span> <span data-ttu-id="5ff3f-117">*lParam2* é zero.</span><span class="sxs-lookup"><span data-stu-id="5ff3f-117">*lParam2* is zero.</span></span>          |
| <span data-ttu-id="5ff3f-118">WMT \_ fechado</span><span class="sxs-lookup"><span data-stu-id="5ff3f-118">WMT\_CLOSED</span></span>          | <span data-ttu-id="5ff3f-119">A indexação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="5ff3f-119">Indexing has been completed.</span></span> <span data-ttu-id="5ff3f-120">*lParam2* é zero.</span><span class="sxs-lookup"><span data-stu-id="5ff3f-120">*lParam2* is zero.</span></span> |
| <span data-ttu-id="5ff3f-121">\_progresso do índice de WMT \_</span><span class="sxs-lookup"><span data-stu-id="5ff3f-121">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="5ff3f-122">A indexação está em andamento.</span><span class="sxs-lookup"><span data-stu-id="5ff3f-122">Indexing is in progress.</span></span>                        |



 

<span data-ttu-id="5ff3f-123">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="5ff3f-123">*lParam2*</span></span>

<span data-ttu-id="5ff3f-124">Se *lParam1* for WMT \_ Closed ou WMT \_ iniciado, *lParam2* será zero.</span><span class="sxs-lookup"><span data-stu-id="5ff3f-124">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="5ff3f-125">Se *lParam1* for WMT \_ index \_ Progress, *lParam2* será um **DWORD** que expressa a quantidade de progresso como uma porcentagem do tamanho total do download.</span><span class="sxs-lookup"><span data-stu-id="5ff3f-125">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that expresses the amount of progress as a percentage of the total download size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ff3f-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ff3f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ff3f-127">**Referência do QASF do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="5ff3f-127">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 




