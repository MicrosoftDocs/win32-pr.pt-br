---
title: Mensagem de MCM_GETMINREQRECT (commctrl. h)
description: Recupera o tamanho mínimo necessário para exibir um mês inteiro em um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- Controles de MCM_GETMINREQRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454931"
---
# <a name="mcm_getminreqrect-message"></a><span data-ttu-id="a27a2-105">\_Mensagem MCM GETMINREQRECT</span><span class="sxs-lookup"><span data-stu-id="a27a2-105">MCM\_GETMINREQRECT message</span></span>

<span data-ttu-id="a27a2-106">Recupera o tamanho mínimo necessário para exibir um mês inteiro em um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="a27a2-106">Retrieves the minimum size required to display a full month in a month calendar control.</span></span> <span data-ttu-id="a27a2-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) .</span><span class="sxs-lookup"><span data-stu-id="a27a2-107">You can send this message explicitly or by using the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a27a2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a27a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a27a2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a27a2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a27a2-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a27a2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a27a2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a27a2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a27a2-112">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá informações de retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="a27a2-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive bounding rectangle information.</span></span> <span data-ttu-id="a27a2-113">Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a27a2-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a27a2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a27a2-114">Return value</span></span>

<span data-ttu-id="a27a2-115">Retorna zero e *lParam* recebe as informações delimitadoras aplicáveis, se bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="a27a2-115">Returns nonzero and *lParam* receives the applicable bounding information if successful.</span></span> <span data-ttu-id="a27a2-116">Caso contrário, a mensagem retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a27a2-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a27a2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a27a2-117">Remarks</span></span>

<span data-ttu-id="a27a2-118">O tamanho mínimo necessário da janela para um controle de calendário mensal depende da fonte atualmente selecionada, dos estilos de controle, das métricas do sistema e das configurações regionais.</span><span class="sxs-lookup"><span data-stu-id="a27a2-118">The minimum required window size for a month calendar control depends on the currently selected font, control styles, system metrics, and regional settings.</span></span> <span data-ttu-id="a27a2-119">Quando um aplicativo altera qualquer coisa que afete o tamanho mínimo da janela ou processa uma mensagem do [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) , ele deve enviar **MCM \_ GETMINREQRECT** para determinar o novo tamanho mínimo.</span><span class="sxs-lookup"><span data-stu-id="a27a2-119">When an application changes anything that affects the minimum window size, or processes a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message, it should send **MCM\_GETMINREQRECT** to determine the new minimum size.</span></span>

> [!Note]  
> <span data-ttu-id="a27a2-120">O retângulo retornado por **MCM \_ GETMINREQRECT** não inclui a largura da cadeia de caracteres "Today", se estiver presente.</span><span class="sxs-lookup"><span data-stu-id="a27a2-120">The rectangle returned by **MCM\_GETMINREQRECT** does not include the width of the "Today" string, if it is present.</span></span> <span data-ttu-id="a27a2-121">Se o estilo [**MCS \_ nohoje**](month-calendar-control-styles.md) não estiver definido, seu aplicativo também deverá recuperar o retângulo que define a largura da cadeia de caracteres "hoje" enviando uma mensagem [**MCM \_ GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) .</span><span class="sxs-lookup"><span data-stu-id="a27a2-121">If the [**MCS\_NOTODAY**](month-calendar-control-styles.md) style is not set, your application should also retrieve the rectangle that defines the "Today" string width by sending a [**MCM\_GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) message.</span></span> <span data-ttu-id="a27a2-122">Use o maior dos dois retângulos para garantir que a cadeia de caracteres "hoje" não seja recortada.</span><span class="sxs-lookup"><span data-stu-id="a27a2-122">Use the larger of the two rectangles to ensure that the "Today" string is not clipped.</span></span>

 

<span data-ttu-id="a27a2-123">Os membros **superior** e **esquerdo** da estrutura apontados por *lParam* serão sempre zero.</span><span class="sxs-lookup"><span data-stu-id="a27a2-123">The **top** and **left** members of the structure pointed to by *lParam* will always be zero.</span></span> <span data-ttu-id="a27a2-124">Os membros **direito** e **inferior** representam o mínimo de *CX* e *CY* necessários para o controle.</span><span class="sxs-lookup"><span data-stu-id="a27a2-124">The **right** and **bottom** members represent the minimum *cx* and *cy* required for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a27a2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a27a2-125">Requirements</span></span>



| <span data-ttu-id="a27a2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a27a2-126">Requirement</span></span> | <span data-ttu-id="a27a2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a27a2-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a27a2-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a27a2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a27a2-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a27a2-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a27a2-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a27a2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a27a2-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a27a2-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a27a2-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a27a2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a27a2-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a27a2-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

