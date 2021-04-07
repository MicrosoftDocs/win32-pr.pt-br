---
title: Mensagem de TBM_GETCHANNELRECT (commctrl. h)
description: Recupera o tamanho e a posição do retângulo delimitador para o canal de um TrackBar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- Controles de TBM_GETCHANNELRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918163"
---
# <a name="tbm_getchannelrect-message"></a><span data-ttu-id="08d33-104">\_Mensagem tbm GETCHANNELRECT</span><span class="sxs-lookup"><span data-stu-id="08d33-104">TBM\_GETCHANNELRECT message</span></span>

<span data-ttu-id="08d33-105">Recupera o tamanho e a posição do retângulo delimitador para o canal de um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="08d33-105">Retrieves the size and position of the bounding rectangle for a trackbar's channel.</span></span> <span data-ttu-id="08d33-106">(O canal é a área sobre a qual o controle deslizante se move.</span><span class="sxs-lookup"><span data-stu-id="08d33-106">(The channel is the area over which the slider moves.</span></span> <span data-ttu-id="08d33-107">Ele contém o realce quando um intervalo é selecionado.)</span><span class="sxs-lookup"><span data-stu-id="08d33-107">It contains the highlight when a range is selected.)</span></span>

## <a name="parameters"></a><span data-ttu-id="08d33-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08d33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d33-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08d33-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="08d33-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="08d33-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="08d33-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08d33-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08d33-112">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="08d33-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="08d33-113">A mensagem preenche essa estrutura com o retângulo delimitador do canal, nas coordenadas do cliente da janela do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="08d33-113">The message fills this structure with the channel's bounding rectangle, in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d33-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08d33-114">Return value</span></span>

<span data-ttu-id="08d33-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="08d33-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d33-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08d33-116">Requirements</span></span>



| <span data-ttu-id="08d33-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="08d33-117">Requirement</span></span> | <span data-ttu-id="08d33-118">Valor</span><span class="sxs-lookup"><span data-stu-id="08d33-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08d33-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08d33-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08d33-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08d33-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08d33-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08d33-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08d33-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08d33-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08d33-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08d33-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08d33-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08d33-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

