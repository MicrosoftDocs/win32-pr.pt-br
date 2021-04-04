---
title: EN_CORRECTTEXT código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que ocorreu um gesto de SYV \_ correto, dando à janela pai a oportunidade de cancelar a correção do texto. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085214"
---
# <a name="en_correcttext-notification-code"></a><span data-ttu-id="d98bb-105">\_Código de notificação en CORRECTTEXT</span><span class="sxs-lookup"><span data-stu-id="d98bb-105">EN\_CORRECTTEXT notification code</span></span>

<span data-ttu-id="d98bb-106">Notifica uma janela pai do controle de edição rico que ocorreu um gesto de SYV \_ correto, dando à janela pai a oportunidade de cancelar a correção do texto.</span><span class="sxs-lookup"><span data-stu-id="d98bb-106">Notifies a rich edit control parent window that a SYV\_CORRECT gesture occurred, giving the parent window a chance to cancel correcting the text.</span></span> <span data-ttu-id="d98bb-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d98bb-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d98bb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d98bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d98bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d98bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d98bb-110">Uma estrutura [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) que especifica a seleção a ser corrigida.</span><span class="sxs-lookup"><span data-stu-id="d98bb-110">An [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) structure specifying the selection to be corrected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d98bb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d98bb-111">Return value</span></span>

<span data-ttu-id="d98bb-112">Retornar zero para ignorar a ação.</span><span class="sxs-lookup"><span data-stu-id="d98bb-112">Return zero to ignore the action.</span></span>

<span data-ttu-id="d98bb-113">Retorna um valor diferente de zero para processar a ação.</span><span class="sxs-lookup"><span data-stu-id="d98bb-113">Returns a nonzero value to process the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="d98bb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d98bb-114">Remarks</span></span>

<span data-ttu-id="d98bb-115">Esse código de notificação será enviado somente se os recursos de caneta estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d98bb-115">This notification code is sent only if pen capabilities are available.</span></span>

<span data-ttu-id="d98bb-116">Para receber \_ códigos de notificação do en CORRECTTEXT, especifique [**enm \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d98bb-116">To receive EN\_CORRECTTEXT notification codes, specify [**ENM\_CORRECTTEXT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="d98bb-117">O \_ código de notificação en CORRECTTEXT só tem suporte na versão de edição avançada 1,0.</span><span class="sxs-lookup"><span data-stu-id="d98bb-117">The EN\_CORRECTTEXT notification code is only supported in rich edit version 1.0.</span></span> <span data-ttu-id="d98bb-118">Não há suporte para ele em versões posteriores do rich edit.</span><span class="sxs-lookup"><span data-stu-id="d98bb-118">It is not supported in later versions of rich edit.</span></span> <span data-ttu-id="d98bb-119">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d98bb-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d98bb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d98bb-120">Requirements</span></span>



| <span data-ttu-id="d98bb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d98bb-121">Requirement</span></span> | <span data-ttu-id="d98bb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d98bb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d98bb-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d98bb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d98bb-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d98bb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d98bb-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d98bb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d98bb-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d98bb-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d98bb-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d98bb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d98bb-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d98bb-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d98bb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d98bb-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d98bb-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d98bb-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d98bb-131">**ENCORRECTTEXT**</span><span class="sxs-lookup"><span data-stu-id="d98bb-131">**ENCORRECTTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





