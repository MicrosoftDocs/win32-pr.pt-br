---
title: Mensagem de EM_EXLIMITTEXT (RichEdit. h)
description: Define um limite superior para a quantidade de texto que o usuário pode digitar ou colar em um controle de edição rico.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- Controles de EM_EXLIMITTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455440"
---
# <a name="em_exlimittext-message"></a><span data-ttu-id="c73b0-104">\_Mensagem em EXLIMITTEXT</span><span class="sxs-lookup"><span data-stu-id="c73b0-104">EM\_EXLIMITTEXT message</span></span>

<span data-ttu-id="c73b0-105">Define um limite superior para a quantidade de texto que o usuário pode digitar ou colar em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="c73b0-105">Sets an upper limit to the amount of text the user can type or paste into a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c73b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c73b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c73b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c73b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c73b0-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c73b0-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c73b0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c73b0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c73b0-110">Especifica a quantidade máxima de texto que pode ser inserida.</span><span class="sxs-lookup"><span data-stu-id="c73b0-110">Specifies the maximum amount of text that can be entered.</span></span> <span data-ttu-id="c73b0-111">Se esse parâmetro for zero, o máximo padrão será usado, que é de 64K caracteres.</span><span class="sxs-lookup"><span data-stu-id="c73b0-111">If this parameter is zero, the default maximum is used, which is 64K characters.</span></span> <span data-ttu-id="c73b0-112">Um objeto COM conta como um único caractere.</span><span class="sxs-lookup"><span data-stu-id="c73b0-112">A COM object counts as a single character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c73b0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c73b0-113">Return value</span></span>

<span data-ttu-id="c73b0-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c73b0-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c73b0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c73b0-115">Remarks</span></span>

<span data-ttu-id="c73b0-116">O limite de texto definido pela mensagem em **\_ EXLIMITTEXT** não limita a quantidade de texto que você pode transmitir em um controle de edição rico usando a mensagem de [**\_ fluxo**](em-streamin.md) em em com *lParam* definido como \_ SMS.</span><span class="sxs-lookup"><span data-stu-id="c73b0-116">The text limit set by the **EM\_EXLIMITTEXT** message does not limit the amount of text that you can stream into a rich edit control using the [**EM\_STREAMIN**](em-streamin.md) message with *lParam* set to SF\_TEXT.</span></span> <span data-ttu-id="c73b0-117">No entanto, ele limita a quantidade de texto que você pode transmitir em um controle de edição rico usando a mensagem de **\_ fluxo** em em com *lParam* definido como it \_ RTF.</span><span class="sxs-lookup"><span data-stu-id="c73b0-117">However, it does limit the amount of text that you can stream into a rich edit control using the **EM\_STREAMIN** message with *lParam* set to SF\_RTF.</span></span>

<span data-ttu-id="c73b0-118">Antes **de \_ EXLIMITTEXT** ser chamado, o limite padrão para a quantidade de texto que um usuário pode inserir é de 32.767 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c73b0-118">Before **EM\_EXLIMITTEXT** is called, the default limit to the amount of text a user can enter is 32,767 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c73b0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c73b0-119">Requirements</span></span>



| <span data-ttu-id="c73b0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c73b0-120">Requirement</span></span> | <span data-ttu-id="c73b0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c73b0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c73b0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c73b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c73b0-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c73b0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c73b0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c73b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c73b0-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c73b0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c73b0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c73b0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c73b0-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c73b0-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c73b0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c73b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c73b0-129">**fluxo de em \_**</span><span class="sxs-lookup"><span data-stu-id="c73b0-129">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





