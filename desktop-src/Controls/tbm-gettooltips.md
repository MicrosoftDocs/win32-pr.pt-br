---
title: Mensagem de TBM_GETTOOLTIPS (commctrl. h)
description: Recupera o identificador para o controle de dica de ferramenta atribuído ao TrackBar, se houver.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- Controles de TBM_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824422"
---
# <a name="tbm_gettooltips-message"></a><span data-ttu-id="af38c-104">\_Mensagem tbm GETtooltips</span><span class="sxs-lookup"><span data-stu-id="af38c-104">TBM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="af38c-105">Recupera o identificador para o controle de dica de ferramenta atribuído ao TrackBar, se houver.</span><span class="sxs-lookup"><span data-stu-id="af38c-105">Retrieves the handle to the tooltip control assigned to the trackbar, if any.</span></span>

## <a name="parameters"></a><span data-ttu-id="af38c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af38c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af38c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af38c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="af38c-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="af38c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="af38c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af38c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="af38c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="af38c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af38c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af38c-111">Return value</span></span>

<span data-ttu-id="af38c-112">Retorna o identificador para o controle de dica de ferramenta atribuído ao TrackBar, ou **NULL** se as dicas de ferramentas não estiverem em uso.</span><span class="sxs-lookup"><span data-stu-id="af38c-112">Returns the handle to the tooltip control assigned to the trackbar, or **NULL** if tooltips are not in use.</span></span> <span data-ttu-id="af38c-113">Se o controle TrackBar não usar o estilo [**de \_ dicas de ferramenta TBS**](trackbar-control-styles.md) , o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="af38c-113">If the trackbar control does not use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="af38c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af38c-114">Requirements</span></span>



| <span data-ttu-id="af38c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="af38c-115">Requirement</span></span> | <span data-ttu-id="af38c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="af38c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af38c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af38c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af38c-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af38c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af38c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af38c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af38c-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af38c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af38c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af38c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="af38c-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="af38c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





