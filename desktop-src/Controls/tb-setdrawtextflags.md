---
title: Mensagem de TB_SETDRAWTEXTFLAGS (commctrl. h)
description: Define os sinalizadores de desenho de texto para a barra de ferramentas.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- Controles de TB_SETDRAWTEXTFLAGS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918858"
---
# <a name="tb_setdrawtextflags-message"></a><span data-ttu-id="2c7a2-104">TB de \_ mensagem SETDRAWTEXTFLAGS</span><span class="sxs-lookup"><span data-stu-id="2c7a2-104">TB\_SETDRAWTEXTFLAGS message</span></span>

<span data-ttu-id="2c7a2-105">Define os sinalizadores de desenho de texto para a barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-105">Sets the text drawing flags for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c7a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c7a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c7a2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c7a2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c7a2-108">Um ou mais dos sinalizadores DT \_ , especificados em [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), que indicam quais bits em *lParam* serão usados ao desenhar o texto.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-108">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate which bits in *lParam* will be used when drawing the text.</span></span>

</dd> <dt>

<span data-ttu-id="2c7a2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c7a2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c7a2-110">Um ou mais dos sinalizadores DT \_ , especificados em [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), que indicam como o texto do botão será desenhado.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-110">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate how the button text will be drawn.</span></span> <span data-ttu-id="2c7a2-111">Esse valor será passado para a função **DrawText** quando o texto do botão for desenhado.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-111">This value will be passed to the **DrawText** function when the button text is drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c7a2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c7a2-112">Return value</span></span>

<span data-ttu-id="2c7a2-113">Retorna os sinalizadores de desenho de texto anteriores.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-113">Returns the previous text drawing flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c7a2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c7a2-114">Remarks</span></span>

<span data-ttu-id="2c7a2-115">O parâmetro *wParam* permite que você especifique quais sinalizadores serão usados ao desenhar o texto, mesmo se esses sinalizadores estiverem desativados.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-115">The *wParam* parameter allows you to specify which flags will be used when drawing the text, even if these flags are turned off.</span></span> <span data-ttu-id="2c7a2-116">Por exemplo, se você não quiser que o sinalizador do centro de DT seja \_ usado ao desenhar o texto, você adicionaria o sinalizador do centro de DT \_ a *wParam* e não especificaria o sinalizador do centro de DT \_ em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2c7a2-116">For example, if you do not want the DT\_CENTER flag used when drawing text, you would add the DT\_CENTER flag to *wParam* and not specify the DT\_CENTER flag in *lParam*.</span></span> <span data-ttu-id="2c7a2-117">Isso impede que o controle passe o sinalizador do centro de DT \_ para a função [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="2c7a2-117">This prevents the control from passing the DT\_CENTER flag to the [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c7a2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c7a2-118">Requirements</span></span>



| <span data-ttu-id="2c7a2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c7a2-119">Requirement</span></span> | <span data-ttu-id="2c7a2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2c7a2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7a2-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c7a2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2c7a2-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c7a2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c7a2-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c7a2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2c7a2-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c7a2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c7a2-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c7a2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c7a2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c7a2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

