---
title: Mensagem de LB_SETTABSTOPS (WinUser. h)
description: Define as posições de parada de tabulação em uma caixa de listagem.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- Controles de LB_SETTABSTOPS de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824674"
---
# <a name="lb_settabstops-message"></a><span data-ttu-id="2bd3f-104">Mensagem do LB \_ SETtabstops</span><span class="sxs-lookup"><span data-stu-id="2bd3f-104">LB\_SETTABSTOPS message</span></span>

<span data-ttu-id="2bd3f-105">Define as posições de parada de tabulação em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-105">Sets the tab-stop positions in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="2bd3f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bd3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bd3f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2bd3f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd3f-108">Especifica o número de paradas de tabulação.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-108">Specifies the number of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="2bd3f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2bd3f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd3f-110">Ponteiro para o primeiro membro de uma matriz de inteiros contendo as paradas de tabulação.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-110">Pointer to the first member of an array of integers containing the tab stops.</span></span> <span data-ttu-id="2bd3f-111">Os inteiros representam o número de trimestres da largura média de caracteres da fonte selecionada na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-111">The integers represent the number of quarters of the average character width for the font that is selected into the list box.</span></span> <span data-ttu-id="2bd3f-112">Por exemplo, uma parada de tabulação de 4 é colocada em 1,0 unidades de caracteres e uma parada de tabulação de 6 é colocada em unidades de caracteres médias de 1,5.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-112">For example, a tab stop of 4 is placed at 1.0 character units, and a tab stop of 6 is placed at 1.5 average character units.</span></span> <span data-ttu-id="2bd3f-113">No entanto, se a caixa de listagem fizer parte de uma caixa de diálogo, os inteiros estarão em unidades de modelo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-113">However, if the list box is part of a dialog box, the integers are in dialog template units.</span></span> <span data-ttu-id="2bd3f-114">As paradas de tabulação devem ser classificadas em ordem crescente; Não são permitidas guias regressivas.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-114">The tab stops must be sorted in ascending order; backward tabs are not allowed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bd3f-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2bd3f-115">Return value</span></span>

<span data-ttu-id="2bd3f-116">Se todas as guias especificadas forem definidas, o valor de retorno será **true**; caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-116">If all the specified tabs are set, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd3f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bd3f-117">Remarks</span></span>

<span data-ttu-id="2bd3f-118">Para responder à mensagem do **lb \_ SetTabStops** , a caixa de listagem deve ter sido criada com o estilo [**lbs \_ USETABSTOPS**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd3f-118">To respond to the **LB\_SETTABSTOPS** message, the list box must have been created with the [**LBS\_USETABSTOPS**](list-box-styles.md) style.</span></span>

<span data-ttu-id="2bd3f-119">Se *wParam* for 0 e *lParam* for **NULL**, a parada de tabulação padrão será de duas unidades de modelo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-119">If *wParam* is 0 and *lParam* is **NULL**, the default tab stop is two dialog template units.</span></span> <span data-ttu-id="2bd3f-120">Se *wParam* for 1, a caixa de listagem terá paradas de tabulação separadas pela distância especificada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-120">If *wParam* is 1, the list box will have tab stops separated by the distance specified by *lParam*.</span></span>

<span data-ttu-id="2bd3f-121">Se *lParam* apontar para mais de um único valor, uma parada de tabulação será definida para cada valor em *lParam*, até o número especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-121">If *lParam* points to more than a single value, a tab stop will be set for each value in *lParam*, up to the number specified by *wParam*.</span></span>

<span data-ttu-id="2bd3f-122">Os valores especificados por *lParam* estão em unidades de modelo de caixa de diálogo, que são as unidades independentes de dispositivo usadas em modelos de caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-122">The values specified by *lParam* are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="2bd3f-123">Para converter medidas de unidades de modelo de caixa de diálogo em unidades de tela (pixels), use a função [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="2bd3f-123">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="2bd3f-124">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o buffer apontado por *lParam* deve residir na memória gravável, embora a mensagem não modifique a matriz.</span><span class="sxs-lookup"><span data-stu-id="2bd3f-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The buffer pointed to by *lParam* must reside in writable memory, even though the message does not modify the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd3f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bd3f-125">Requirements</span></span>



| <span data-ttu-id="2bd3f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd3f-126">Requirement</span></span> | <span data-ttu-id="2bd3f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2bd3f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd3f-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bd3f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd3f-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2bd3f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2bd3f-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bd3f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd3f-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2bd3f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2bd3f-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2bd3f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd3f-133"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bd3f-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd3f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bd3f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd3f-135">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="2bd3f-135">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

