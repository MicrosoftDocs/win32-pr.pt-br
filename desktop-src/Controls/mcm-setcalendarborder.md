---
title: Mensagem de MCM_SETCALENDARBORDER (commctrl. h)
description: Define o tamanho da borda, em pixels. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- Controles de MCM_SETCALENDARBORDER de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455116"
---
# <a name="mcm_setcalendarborder-message"></a><span data-ttu-id="d4ec6-105">\_Mensagem MCM SETCALENDARBORDER</span><span class="sxs-lookup"><span data-stu-id="d4ec6-105">MCM\_SETCALENDARBORDER message</span></span>

<span data-ttu-id="d4ec6-106">Define o tamanho da borda, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d4ec6-106">Sets the size of the border, in pixels.</span></span> <span data-ttu-id="d4ec6-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .</span><span class="sxs-lookup"><span data-stu-id="d4ec6-107">You can send this message explicitly or by using the [**MonthCal\_SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4ec6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4ec6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ec6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4ec6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ec6-110">Se for **true**, o tamanho da borda será definido como o número de pixels especificado por *lParam* .</span><span class="sxs-lookup"><span data-stu-id="d4ec6-110">If **TRUE**, then the border size is set to the number of pixels that *lParam* specifies.</span></span> <span data-ttu-id="d4ec6-111">Se **for false**, o tamanho da borda será redefinido para o valor padrão especificado pelo tema ou zero se os temas não estiverem sendo usados.</span><span class="sxs-lookup"><span data-stu-id="d4ec6-111">If **FALSE**, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4ec6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ec6-113">Número de pixels do tamanho da borda.</span><span class="sxs-lookup"><span data-stu-id="d4ec6-113">Number of pixels of the border size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ec6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4ec6-114">Return value</span></span>

<span data-ttu-id="d4ec6-115">Não usado.</span><span class="sxs-lookup"><span data-stu-id="d4ec6-115">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ec6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4ec6-116">Requirements</span></span>



| <span data-ttu-id="d4ec6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4ec6-117">Requirement</span></span> | <span data-ttu-id="d4ec6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d4ec6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ec6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4ec6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ec6-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4ec6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4ec6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4ec6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ec6-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d4ec6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4ec6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4ec6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ec6-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ec6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





