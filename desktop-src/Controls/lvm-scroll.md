---
title: Mensagem de LVM_SCROLL (commctrl. h)
description: Rola o conteúdo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ rolagem de ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- Controles de LVM_SCROLL de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455427"
---
# <a name="lvm_scroll-message"></a><span data-ttu-id="7ccb4-105">\_Mensagem de rolagem LVM</span><span class="sxs-lookup"><span data-stu-id="7ccb4-105">LVM\_SCROLL message</span></span>

<span data-ttu-id="7ccb4-106">Rola o conteúdo de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-106">Scrolls the content of a list-view control.</span></span> <span data-ttu-id="7ccb4-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ rolagem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) .</span><span class="sxs-lookup"><span data-stu-id="7ccb4-107">You can send this message explicitly or by using the [**ListView\_Scroll**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ccb4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ccb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ccb4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ccb4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ccb4-110">Valor do tipo **int** que especifica a quantidade de rolagem horizontal, em pixels, relativa à posição atual do conteúdo da exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-110">Value of type **int** that specifies the amount of horizontal scrolling, in pixels, relative to the current position of the list view content.</span></span> <span data-ttu-id="7ccb4-111">Se o controle de exibição de lista estiver no modo de exibição de lista, esse valor será arredondado para o número mais próximo de pixels que formam uma coluna inteira.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-111">If the list-view control is in list view, this value is rounded up to the nearest number of pixels that form a whole column.</span></span>

</dd> <dt>

<span data-ttu-id="7ccb4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ccb4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ccb4-113">Valor do tipo **int** que especifica a quantidade de rolagem vertical, em pixels, relativa à posição atual do conteúdo da exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-113">Value of type **int** that specifies the amount of vertical scrolling, in pixels, relative to the current position of the list view content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ccb4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ccb4-114">Return value</span></span>

<span data-ttu-id="7ccb4-115">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-115">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ccb4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ccb4-116">Remarks</span></span>

<span data-ttu-id="7ccb4-117">Quando o controle de exibição de lista está no modo de exibição de relatório, o controle só pode ser rolado verticalmente em incrementos de linha inteira.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-117">When the list-view control is in report view, the control can only be scrolled vertically in whole line increments.</span></span> <span data-ttu-id="7ccb4-118">Portanto, o parâmetro *lParam* será arredondado para o número mais próximo de pixels que formam um incremento de linha inteiro.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-118">Therefore, the *lParam* parameter will be rounded to the nearest number of pixels that form a whole line increment.</span></span> <span data-ttu-id="7ccb4-119">Por exemplo, se a altura de uma linha for de 16 pixels e 8 for passada para *lParam*, a lista será rolada por 16 pixels (1 linha).</span><span class="sxs-lookup"><span data-stu-id="7ccb4-119">For example, if the height of a line is 16 pixels and 8 is passed for *lParam*, the list will be scrolled by 16 pixels (1 line).</span></span> <span data-ttu-id="7ccb4-120">Se 7 for passado para *lParam*, a lista será rolada em 0 pixels (0 linhas).</span><span class="sxs-lookup"><span data-stu-id="7ccb4-120">If 7 is passed for *lParam*, the list will be scrolled 0 pixels (0 lines).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ccb4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ccb4-121">Requirements</span></span>



| <span data-ttu-id="7ccb4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ccb4-122">Requirement</span></span> | <span data-ttu-id="7ccb4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7ccb4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccb4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ccb4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7ccb4-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ccb4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ccb4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ccb4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7ccb4-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ccb4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ccb4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ccb4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ccb4-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ccb4-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





