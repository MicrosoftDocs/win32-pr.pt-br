---
title: Mensagem de EM_SHOWSCROLLBAR (RichEdit. h)
description: Mostra ou oculta uma das barras de rolagem na janela host de um controle rich edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- Controles de EM_SHOWSCROLLBAR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918346"
---
# <a name="em_showscrollbar-message"></a><span data-ttu-id="15a89-104">Na \_ mensagem de ScrollBar</span><span class="sxs-lookup"><span data-stu-id="15a89-104">EM\_SHOWSCROLLBAR message</span></span>

<span data-ttu-id="15a89-105">Mostra ou oculta uma das barras de rolagem na janela host de um controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="15a89-105">Shows or hides one of the scroll bars in the host window of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="15a89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15a89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a89-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15a89-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15a89-108">Identifica a barra de rolagem a ser exibida: horizontal ou vertical.</span><span class="sxs-lookup"><span data-stu-id="15a89-108">Identifies which scroll bar to display: horizontal or vertical.</span></span> <span data-ttu-id="15a89-109">Esse parâmetro deve ser **SB \_ Vert** ou **SB \_ na horizontal**.</span><span class="sxs-lookup"><span data-stu-id="15a89-109">This parameter must be **SB\_VERT** or **SB\_HORZ**.</span></span>

</dd> <dt>

<span data-ttu-id="15a89-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15a89-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15a89-111">Especifica se a barra de rolagem deve ser mostrada ou ocultada.</span><span class="sxs-lookup"><span data-stu-id="15a89-111">Specifies whether to show the scroll bar or hide it.</span></span> <span data-ttu-id="15a89-112">Especifique **true** para mostrar a barra de rolagem e **false** para ocultá-la.</span><span class="sxs-lookup"><span data-stu-id="15a89-112">Specify **TRUE** to show the scroll bar and **FALSE** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a89-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15a89-113">Return value</span></span>

<span data-ttu-id="15a89-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="15a89-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a89-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="15a89-115">Remarks</span></span>

<span data-ttu-id="15a89-116">Esse método só é válido quando o controle está ativo no local.</span><span class="sxs-lookup"><span data-stu-id="15a89-116">This method is only valid when the control is in-place active.</span></span> <span data-ttu-id="15a89-117">As chamadas feitas enquanto o controle estiver inativo pode falhar.</span><span class="sxs-lookup"><span data-stu-id="15a89-117">Calls made while the control is inactive may fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a89-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15a89-118">Requirements</span></span>



| <span data-ttu-id="15a89-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="15a89-119">Requirement</span></span> | <span data-ttu-id="15a89-120">Valor</span><span class="sxs-lookup"><span data-stu-id="15a89-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15a89-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15a89-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15a89-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15a89-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15a89-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15a89-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15a89-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="15a89-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15a89-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15a89-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15a89-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="15a89-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a89-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="15a89-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="15a89-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="15a89-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="15a89-129">**em \_ GETSCROLLPOS**</span><span class="sxs-lookup"><span data-stu-id="15a89-129">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> <dt>

[<span data-ttu-id="15a89-130">**em \_ SETSCROLLPOS**</span><span class="sxs-lookup"><span data-stu-id="15a89-130">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

 





