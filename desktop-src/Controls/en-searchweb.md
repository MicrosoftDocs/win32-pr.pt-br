---
title: EN_SEARCHWEB código de notificação (CommCtrl. h)
description: Enviado quando um controle de edição perde o foco do teclado. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de notificação do WM \_ .
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454703"
---
# <a name="en_searchweb-notification-code"></a><span data-ttu-id="dfff6-105">\_Código de notificação en SEARCHWEB</span><span class="sxs-lookup"><span data-stu-id="dfff6-105">EN\_SEARCHWEB notification code</span></span>

<span data-ttu-id="dfff6-106">Enviado depois que um controle de edição realizou uma pesquisa na Web quando o recurso "Pesquisar na Web" estiver habilitado, consulte [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span><span class="sxs-lookup"><span data-stu-id="dfff6-106">Sent after an edit control performed a web search when the "Search the web" feature is enabled, see [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span></span> <span data-ttu-id="dfff6-107">A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="dfff6-107">The parent window of the edit control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="dfff6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfff6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfff6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dfff6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfff6-110">Identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="dfff6-110">Handle to the edit control.</span></span>

</dd> <dt>

<span data-ttu-id="dfff6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dfff6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfff6-112">Um ponteiro para uma estrutura [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .</span><span class="sxs-lookup"><span data-stu-id="dfff6-112">A pointer to a [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfff6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfff6-113">Requirements</span></span>



| <span data-ttu-id="dfff6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfff6-114">Requirement</span></span> | <span data-ttu-id="dfff6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dfff6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfff6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfff6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dfff6-117">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="dfff6-117">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dfff6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfff6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dfff6-119">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="dfff6-119">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dfff6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfff6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfff6-121"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfff6-121"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfff6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfff6-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="dfff6-123">**Referência**</span><span class="sxs-lookup"><span data-stu-id="dfff6-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dfff6-124">**em \_ ENABLESEARCHWEB**</span><span class="sxs-lookup"><span data-stu-id="dfff6-124">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> <dt>

<span data-ttu-id="dfff6-125">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="dfff6-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="dfff6-126">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="dfff6-126">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





