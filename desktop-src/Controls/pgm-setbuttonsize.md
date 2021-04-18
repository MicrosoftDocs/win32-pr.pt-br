---
title: Mensagem de PGM_SETBUTTONSIZE (commctrl. h)
description: Define o tamanho do botão atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetButtons do pager.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- Controles de PGM_SETBUTTONSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499330"
---
# <a name="pgm_setbuttonsize-message"></a><span data-ttu-id="fa93a-105">\_Mensagem de SETbuttons do PGM</span><span class="sxs-lookup"><span data-stu-id="fa93a-105">PGM\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="fa93a-106">Define o tamanho do botão atual para o controle de pager.</span><span class="sxs-lookup"><span data-stu-id="fa93a-106">Sets the current button size for the pager control.</span></span> <span data-ttu-id="fa93a-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetButtons do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="fa93a-107">You can send this message explicitly or use the [**Pager\_SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa93a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa93a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa93a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa93a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fa93a-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fa93a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fa93a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa93a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa93a-112">Valor do tipo **int** que contém o novo tamanho do botão, em pixels.</span><span class="sxs-lookup"><span data-stu-id="fa93a-112">Value of type **int** that contains the new button size, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa93a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa93a-113">Return value</span></span>

<span data-ttu-id="fa93a-114">Retorna um valor **int** que contém o tamanho do botão anterior, em pixels.</span><span class="sxs-lookup"><span data-stu-id="fa93a-114">Returns an **int** value that contains the previous button size, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa93a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa93a-115">Remarks</span></span>

<span data-ttu-id="fa93a-116">Se o controle de pager tiver o estilo [**PGS \_ na horizontal**](pager-control-styles.md) , o tamanho do botão determinará a largura dos botões da paginação.</span><span class="sxs-lookup"><span data-stu-id="fa93a-116">If the pager control has the [**PGS\_HORZ**](pager-control-styles.md) style, the button size determines the width of the pager buttons.</span></span> <span data-ttu-id="fa93a-117">Se o controle de pager tiver o estilo [**\_ vertical PGS**](pager-control-styles.md) , o tamanho do botão determinará a altura dos botões da paginação.</span><span class="sxs-lookup"><span data-stu-id="fa93a-117">If the pager control has the [**PGS\_VERT**](pager-control-styles.md) style, the button size determines the height of the pager buttons.</span></span> <span data-ttu-id="fa93a-118">Por padrão, o controle de pager define seu tamanho de botão como três quartos da largura da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="fa93a-118">By default, the pager control sets its button size to three-fourths of the width of the scroll bar.</span></span>

<span data-ttu-id="fa93a-119">Há um tamanho mínimo para o botão de pager, no momento, 12 pixels.</span><span class="sxs-lookup"><span data-stu-id="fa93a-119">There is a minimum size to the pager button, currently 12 pixels.</span></span> <span data-ttu-id="fa93a-120">No entanto, isso pode ser alterado, portanto, você não deve depender desse valor.</span><span class="sxs-lookup"><span data-stu-id="fa93a-120">However, this can change so you should not depend on this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa93a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa93a-121">Requirements</span></span>



| <span data-ttu-id="fa93a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa93a-122">Requirement</span></span> | <span data-ttu-id="fa93a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fa93a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa93a-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa93a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fa93a-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa93a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa93a-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa93a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fa93a-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa93a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa93a-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa93a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa93a-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa93a-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa93a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa93a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa93a-131">**getbuttons do PGM \_**</span><span class="sxs-lookup"><span data-stu-id="fa93a-131">**PGM\_GETBUTTONSIZE**</span></span>](pgm-getbuttonsize.md)
</dt> </dl>

 

 





