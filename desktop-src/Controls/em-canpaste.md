---
title: Mensagem de EM_CANPASTE (RichEdit. h)
description: Determina se um controle de edição rico pode colar um formato de área de transferência especificado.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- Controles de EM_CANPASTE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009529"
---
# <a name="em_canpaste-message"></a><span data-ttu-id="df678-104">\_Mensagem em CANpaste</span><span class="sxs-lookup"><span data-stu-id="df678-104">EM\_CANPASTE message</span></span>

<span data-ttu-id="df678-105">Determina se um controle de edição rico pode colar um formato de área de transferência especificado.</span><span class="sxs-lookup"><span data-stu-id="df678-105">Determines whether a rich edit control can paste a specified clipboard format.</span></span>

## <a name="parameters"></a><span data-ttu-id="df678-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df678-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df678-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df678-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df678-108">Especifica os [formatos da área de transferência](/windows/desktop/dataxchg/clipboard-formats) a serem experimentados.</span><span class="sxs-lookup"><span data-stu-id="df678-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats) to try.</span></span> <span data-ttu-id="df678-109">Para testar qualquer formato atualmente na área de transferência, defina esse parâmetro como zero.</span><span class="sxs-lookup"><span data-stu-id="df678-109">To try any format currently on the clipboard, set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="df678-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df678-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df678-111">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="df678-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df678-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df678-112">Return value</span></span>

<span data-ttu-id="df678-113">Se o formato da área de transferência puder ser colado, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="df678-113">If the clipboard format can be pasted, the return value is a nonzero value.</span></span>

<span data-ttu-id="df678-114">Se o formato da área de transferência não puder ser colado, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="df678-114">If the clipboard format cannot be pasted, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="df678-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df678-115">Requirements</span></span>



| <span data-ttu-id="df678-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="df678-116">Requirement</span></span> | <span data-ttu-id="df678-117">Valor</span><span class="sxs-lookup"><span data-stu-id="df678-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df678-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df678-118">Minimum supported client</span></span><br/> | <span data-ttu-id="df678-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df678-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df678-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df678-120">Minimum supported server</span></span><br/> | <span data-ttu-id="df678-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df678-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df678-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df678-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="df678-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="df678-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df678-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="df678-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df678-125">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="df678-125">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

