---
title: Mensagem de TB_SETCOLORSCHEME (commctrl. h)
description: Define as informações do esquema de cores para o controle ToolBar.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- Controles de TB_SETCOLORSCHEME de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824754"
---
# <a name="tb_setcolorscheme-message"></a><span data-ttu-id="ef912-104">TB de \_ mensagem SETCOLORSCHEME</span><span class="sxs-lookup"><span data-stu-id="ef912-104">TB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="ef912-105">Define as informações do esquema de cores para o controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="ef912-105">Sets the color scheme information for the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef912-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef912-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef912-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef912-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ef912-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ef912-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ef912-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef912-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef912-110">Ponteiro para uma estrutura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que contém as informações do esquema de cores.</span><span class="sxs-lookup"><span data-stu-id="ef912-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef912-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef912-111">Return value</span></span>

<span data-ttu-id="ef912-112">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="ef912-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef912-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef912-113">Remarks</span></span>

<span data-ttu-id="ef912-114">O controle Toolbar usa as informações do esquema de cores ao desenhar os elementos 3-D no controle.</span><span class="sxs-lookup"><span data-stu-id="ef912-114">The toolbar control uses the color scheme information when drawing the 3-D elements in the control.</span></span>

<span data-ttu-id="ef912-115">Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="ef912-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef912-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef912-116">Requirements</span></span>



| <span data-ttu-id="ef912-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef912-117">Requirement</span></span> | <span data-ttu-id="ef912-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ef912-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef912-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef912-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef912-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef912-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef912-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef912-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef912-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef912-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef912-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef912-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef912-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef912-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef912-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef912-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef912-126">**TB de \_ GETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="ef912-126">**TB\_GETCOLORSCHEME**</span></span>](tb-getcolorscheme.md)
</dt> </dl>

 

 





