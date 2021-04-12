---
title: Mensagem de TVM_SETEXTENDEDSTYLE (commctrl. h)
description: Informa o controle de exibição de árvore para definir estilos estendidos. Envie esta mensagem ou use a macro TreeView \_ setextendedattribute.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- Controles de TVM_SETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499434"
---
# <a name="tvm_setextendedstyle-message"></a><span data-ttu-id="c987c-105">\_Mensagem TVM SETextendedattribute</span><span class="sxs-lookup"><span data-stu-id="c987c-105">TVM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="c987c-106">Informa o controle de exibição de árvore para definir estilos estendidos.</span><span class="sxs-lookup"><span data-stu-id="c987c-106">Informs the tree-view control to set extended styles.</span></span> <span data-ttu-id="c987c-107">Envie esta mensagem ou use a macro [**TreeView \_ setextendedattribute**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="c987c-107">Send this message or use the macro [**TreeView\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="c987c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c987c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c987c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c987c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c987c-110">Máscara usada para selecionar os estilos a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="c987c-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="c987c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c987c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c987c-112">Valor que indica o estilo estendido.</span><span class="sxs-lookup"><span data-stu-id="c987c-112">Value that indicates the extended style.</span></span> <span data-ttu-id="c987c-113">Para obter mais informações sobre estilos, consulte [controle de exibição de árvore estilos estendidos](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="c987c-113">For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c987c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c987c-114">Return value</span></span>

<span data-ttu-id="c987c-115">Se essa mensagem tiver sucesso, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c987c-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c987c-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c987c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c987c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c987c-117">Remarks</span></span>

<span data-ttu-id="c987c-118">Os estilos estendidos para um controle de exibição em árvore não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="c987c-118">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="c987c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c987c-119">Requirements</span></span>



| <span data-ttu-id="c987c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c987c-120">Requirement</span></span> | <span data-ttu-id="c987c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c987c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c987c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c987c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c987c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c987c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c987c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c987c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c987c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c987c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c987c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c987c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c987c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c987c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

