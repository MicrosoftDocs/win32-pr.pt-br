---
title: Mensagem de TTM_GETBUBBLESIZE (commctrl. h)
description: Retorna a largura e a altura de um controle ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- Controles de TTM_GETBUBBLESIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085579"
---
# <a name="ttm_getbubblesize-message"></a><span data-ttu-id="6ebcb-104">TTM \_ GETbubbleize mensagem</span><span class="sxs-lookup"><span data-stu-id="6ebcb-104">TTM\_GETBUBBLESIZE message</span></span>

<span data-ttu-id="6ebcb-105">Retorna a largura e a altura de um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="6ebcb-105">Returns the width and height of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ebcb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ebcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ebcb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ebcb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6ebcb-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6ebcb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6ebcb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ebcb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ebcb-110">Ponteiro para a estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="6ebcb-110">Pointer to the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ebcb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ebcb-111">Return value</span></span>

<span data-ttu-id="6ebcb-112">Retorna a largura da dica de ferramenta na palavra inferior e a altura da palavra alta se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6ebcb-112">Returns the width of the tooltip in the low word and the height in the high word if successful.</span></span> <span data-ttu-id="6ebcb-113">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="6ebcb-113">Otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ebcb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ebcb-114">Remarks</span></span>

<span data-ttu-id="6ebcb-115">Se os sinalizadores de faixa de TTF \_ e de TTF \_ absoluto estiverem definidos no membro **UFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) da dica de ferramenta, essa mensagem poderá ser usada para ajudar a posicionar a dica de ferramenta com precisão.</span><span class="sxs-lookup"><span data-stu-id="6ebcb-115">If the TTF\_TRACK and TTF\_ABSOLUTE flags are set in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, this message can be used to help position the tooltip accurately.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ebcb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ebcb-116">Requirements</span></span>



| <span data-ttu-id="6ebcb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ebcb-117">Requirement</span></span> | <span data-ttu-id="6ebcb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ebcb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebcb-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ebcb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ebcb-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ebcb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ebcb-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ebcb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ebcb-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ebcb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ebcb-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ebcb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ebcb-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ebcb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





