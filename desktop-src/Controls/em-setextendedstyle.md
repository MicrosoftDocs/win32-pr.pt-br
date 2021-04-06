---
title: Mensagem de EM_SETEXTENDEDSTYLE (commctrl. h)
description: Informa o controle de edição para definir os estilos estendidos. Envie esta mensagem ou use a macro Edit \_ setextendedattribute.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- Controles de EM_SETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086186"
---
# <a name="em_setextendedstyle-message"></a><span data-ttu-id="d37e6-105">\_Mensagem em SETextendedattributestyle</span><span class="sxs-lookup"><span data-stu-id="d37e6-105">EM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="d37e6-106">Informa o controle de edição para definir os estilos estendidos.</span><span class="sxs-lookup"><span data-stu-id="d37e6-106">Informs the edit control to set extended styles.</span></span> <span data-ttu-id="d37e6-107">Envie esta mensagem ou use a macro [**Edit \_ setextendedattribute**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="d37e6-107">Send this message or use the macro [**Edit\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="d37e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d37e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d37e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d37e6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d37e6-110">Máscara usada para selecionar os estilos a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="d37e6-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="d37e6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d37e6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d37e6-112">Valor que indica o estilo estendido.</span><span class="sxs-lookup"><span data-stu-id="d37e6-112">Value that indicates the extended style.</span></span> <span data-ttu-id="d37e6-113">Para obter mais informações sobre estilos, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d37e6-113">For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d37e6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d37e6-114">Return value</span></span>

<span data-ttu-id="d37e6-115">Se essa mensagem tiver sucesso, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d37e6-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d37e6-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d37e6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d37e6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d37e6-117">Remarks</span></span>

<span data-ttu-id="d37e6-118">Os estilos estendidos para um controle de edição não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="d37e6-118">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="d37e6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d37e6-119">Requirements</span></span>



| <span data-ttu-id="d37e6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d37e6-120">Requirement</span></span> | <span data-ttu-id="d37e6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d37e6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d37e6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d37e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d37e6-123">\[Somente aplicativos da área de trabalho do Windows 10, versão 1809\]</span><span class="sxs-lookup"><span data-stu-id="d37e6-123">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d37e6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d37e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d37e6-125">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="d37e6-125">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d37e6-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d37e6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d37e6-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d37e6-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

