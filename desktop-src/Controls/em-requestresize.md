---
title: Mensagem de EM_REQUESTRESIZE (RichEdit. h)
description: Força um controle de edição rico a enviar um \_ código de notificação en REQUESTRESIZE para sua janela pai.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- Controles de EM_REQUESTRESIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163620"
---
# <a name="em_requestresize-message"></a><span data-ttu-id="7953b-104">\_Mensagem em REQUESTRESIZE</span><span class="sxs-lookup"><span data-stu-id="7953b-104">EM\_REQUESTRESIZE message</span></span>

<span data-ttu-id="7953b-105">Força um controle de edição rico a enviar um código de notificação [**en \_ REQUESTRESIZE**](en-requestresize.md) para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="7953b-105">Forces a rich edit control to send an [**EN\_REQUESTRESIZE**](en-requestresize.md) notification code to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="7953b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7953b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7953b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7953b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7953b-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7953b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7953b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7953b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7953b-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7953b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7953b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7953b-111">Return value</span></span>

<span data-ttu-id="7953b-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7953b-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7953b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7953b-113">Remarks</span></span>

<span data-ttu-id="7953b-114">Essa mensagem é útil durante o processamento de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) para o pai de um controle de edição com formatação inferior.</span><span class="sxs-lookup"><span data-stu-id="7953b-114">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7953b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7953b-115">Requirements</span></span>



| <span data-ttu-id="7953b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7953b-116">Requirement</span></span> | <span data-ttu-id="7953b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7953b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7953b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7953b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7953b-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7953b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7953b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7953b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7953b-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7953b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7953b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7953b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7953b-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7953b-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7953b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7953b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="7953b-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7953b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7953b-126">**REQUESTRESIZE de EN \_**</span><span class="sxs-lookup"><span data-stu-id="7953b-126">**EN\_REQUESTRESIZE**</span></span>](en-requestresize.md)
</dt> <dt>

<span data-ttu-id="7953b-127">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="7953b-127">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7953b-128">**tamanho do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7953b-128">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

