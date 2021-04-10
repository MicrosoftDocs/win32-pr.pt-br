---
title: Mensagem de TBM_GETTHUMBRECT (commctrl. h)
description: Recupera o tamanho e a posição do retângulo delimitador para o controle deslizante em um TrackBar.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- Controles de TBM_GETTHUMBRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009391"
---
# <a name="tbm_getthumbrect-message"></a><span data-ttu-id="cef50-104">\_Mensagem tbm GETTHUMBRECT</span><span class="sxs-lookup"><span data-stu-id="cef50-104">TBM\_GETTHUMBRECT message</span></span>

<span data-ttu-id="cef50-105">Recupera o tamanho e a posição do retângulo delimitador para o controle deslizante em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="cef50-105">Retrieves the size and position of the bounding rectangle for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="cef50-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cef50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cef50-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cef50-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cef50-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cef50-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cef50-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cef50-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cef50-110">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cef50-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="cef50-111">A mensagem preenche essa estrutura com o retângulo delimitador do controle deslizante do TrackBar nas coordenadas do cliente da janela do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="cef50-111">The message fills this structure with the bounding rectangle of the trackbar's slider in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cef50-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cef50-112">Return value</span></span>

<span data-ttu-id="cef50-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="cef50-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef50-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cef50-114">Requirements</span></span>



| <span data-ttu-id="cef50-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cef50-115">Requirement</span></span> | <span data-ttu-id="cef50-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cef50-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cef50-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cef50-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cef50-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cef50-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cef50-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cef50-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cef50-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cef50-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cef50-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cef50-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cef50-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cef50-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

