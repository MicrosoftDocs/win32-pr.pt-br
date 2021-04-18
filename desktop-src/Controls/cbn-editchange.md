---
title: Código de notificação CBN_EDITCHANGE (WinUser. h)
description: Enviado depois que o usuário executou uma ação que pode ter alterado o texto na parte do controle de edição de uma caixa de combinação.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- CBN_EDITCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a661d647d0879b93675563777d77bba2dfe8c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749311"
---
# <a name="cbn_editchange-notification-code"></a><span data-ttu-id="74807-104">Código de notificação do CBN \_ EDITCHANGE</span><span class="sxs-lookup"><span data-stu-id="74807-104">CBN\_EDITCHANGE notification code</span></span>

<span data-ttu-id="74807-105">Enviado depois que o usuário executou uma ação que pode ter alterado o texto na parte do controle de edição de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="74807-105">Sent after the user has taken an action that may have altered the text in the edit control portion of a combo box.</span></span> <span data-ttu-id="74807-106">Ao contrário do código de notificação [CBN \_ EDITUPDATE](cbn-editupdate.md) , esse código de notificação é enviado depois que o sistema atualiza a tela.</span><span class="sxs-lookup"><span data-stu-id="74807-106">Unlike the [CBN\_EDITUPDATE](cbn-editupdate.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="74807-107">A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="74807-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="74807-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74807-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74807-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74807-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74807-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="74807-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="74807-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="74807-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="74807-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74807-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74807-113">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="74807-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74807-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="74807-114">Remarks</span></span>

<span data-ttu-id="74807-115">Se a caixa de combinação tiver o estilo do [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) , esse código de notificação não será enviado.</span><span class="sxs-lookup"><span data-stu-id="74807-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="74807-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74807-116">Requirements</span></span>



| <span data-ttu-id="74807-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="74807-117">Requirement</span></span> | <span data-ttu-id="74807-118">Valor</span><span class="sxs-lookup"><span data-stu-id="74807-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74807-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74807-119">Minimum supported client</span></span><br/> | <span data-ttu-id="74807-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74807-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="74807-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74807-121">Minimum supported server</span></span><br/> | <span data-ttu-id="74807-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74807-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74807-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74807-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="74807-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74807-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74807-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="74807-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="74807-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="74807-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="74807-127">CBN \_ EDITUPDATE</span><span class="sxs-lookup"><span data-stu-id="74807-127">CBN\_EDITUPDATE</span></span>](cbn-editupdate.md)
</dt> <dt>

<span data-ttu-id="74807-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="74807-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="74807-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74807-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="74807-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74807-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="74807-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="74807-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

