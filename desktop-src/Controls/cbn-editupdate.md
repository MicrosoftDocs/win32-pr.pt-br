---
title: Código de notificação CBN_EDITUPDATE (WinUser. h)
description: Enviado quando a parte do controle de edição de uma caixa de combinação está prestes a exibir o texto alterado.
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- CBN_EDITUPDATE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef56b97bf8f4c4aebb4a11383be1b5a1941167b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086424"
---
# <a name="cbn_editupdate-notification-code"></a><span data-ttu-id="2bc5f-104">Código de notificação do CBN \_ EDITUPDATE</span><span class="sxs-lookup"><span data-stu-id="2bc5f-104">CBN\_EDITUPDATE notification code</span></span>

<span data-ttu-id="2bc5f-105">Enviado quando a parte do controle de edição de uma caixa de combinação está prestes a exibir o texto alterado.</span><span class="sxs-lookup"><span data-stu-id="2bc5f-105">Sent when the edit control portion of a combo box is about to display altered text.</span></span> <span data-ttu-id="2bc5f-106">Esse código de notificação é enviado depois que o controle tiver formatado o texto, mas antes de exibir o texto.</span><span class="sxs-lookup"><span data-stu-id="2bc5f-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="2bc5f-107">A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2bc5f-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITUPDATE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2bc5f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bc5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bc5f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2bc5f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bc5f-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="2bc5f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="2bc5f-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="2bc5f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2bc5f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2bc5f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2bc5f-113">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="2bc5f-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bc5f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bc5f-114">Remarks</span></span>

<span data-ttu-id="2bc5f-115">Se a caixa de combinação tiver o estilo do [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) , esse código de notificação não será enviado.</span><span class="sxs-lookup"><span data-stu-id="2bc5f-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc5f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bc5f-116">Requirements</span></span>



| <span data-ttu-id="2bc5f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bc5f-117">Requirement</span></span> | <span data-ttu-id="2bc5f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2bc5f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc5f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bc5f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc5f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2bc5f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2bc5f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bc5f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc5f-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2bc5f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2bc5f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2bc5f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bc5f-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bc5f-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc5f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bc5f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2bc5f-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2bc5f-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2bc5f-127">CBN \_ EDITCHANGE</span><span class="sxs-lookup"><span data-stu-id="2bc5f-127">CBN\_EDITCHANGE</span></span>](cbn-editchange.md)
</dt> <dt>

<span data-ttu-id="2bc5f-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="2bc5f-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2bc5f-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2bc5f-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2bc5f-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2bc5f-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2bc5f-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2bc5f-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

