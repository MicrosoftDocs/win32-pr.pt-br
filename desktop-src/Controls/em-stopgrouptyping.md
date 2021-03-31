---
title: Mensagem de EM_STOPGROUPTYPING (RichEdit. h)
description: Interrompe um controle de edição rico da coleta de ações de digitação adicionais na ação de desfazer atual. O controle armazena a próxima ação de digitação, se houver, em uma nova ação na fila de desfazer.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- Controles de EM_STOPGROUPTYPING de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644583"
---
# <a name="em_stopgrouptyping-message"></a><span data-ttu-id="bf8c4-105">\_Mensagem em STOPGROUPTYPING</span><span class="sxs-lookup"><span data-stu-id="bf8c4-105">EM\_STOPGROUPTYPING message</span></span>

<span data-ttu-id="bf8c4-106">Interrompe um controle de edição rico da coleta de ações de digitação adicionais na ação de desfazer atual.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-106">Stops a rich edit control from collecting additional typing actions into the current undo action.</span></span> <span data-ttu-id="bf8c4-107">O controle armazena a próxima ação de digitação, se houver, em uma nova ação na fila de desfazer.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-107">The control stores the next typing action, if any, into a new action in the undo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf8c4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf8c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf8c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf8c4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf8c4-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bf8c4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf8c4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf8c4-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf8c4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf8c4-113">Return value</span></span>

<span data-ttu-id="bf8c4-114">O valor de retorno é zero.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-114">The return value is zero.</span></span> <span data-ttu-id="bf8c4-115">Esta mensagem não pode falhar.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-115">This message cannot fail.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf8c4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf8c4-116">Remarks</span></span>

<span data-ttu-id="bf8c4-117">Um controle de edição rico agrupa ações de digitação consecutivas, incluindo caracteres excluídos usando a tecla **Backspace** , em uma única ação desfazer até que um dos seguintes eventos ocorra:</span><span class="sxs-lookup"><span data-stu-id="bf8c4-117">A rich edit control groups consecutive typing actions, including characters deleted by using the **BackSpace** key, into a single undo action until one of the following events occurs:</span></span>

-   <span data-ttu-id="bf8c4-118">O controle recebe uma mensagem em **\_ STOPGROUPTYPING** .</span><span class="sxs-lookup"><span data-stu-id="bf8c4-118">The control receives an **EM\_STOPGROUPTYPING** message.</span></span>
-   <span data-ttu-id="bf8c4-119">O controle perde o foco.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-119">The control loses focus.</span></span>
-   <span data-ttu-id="bf8c4-120">O usuário move a seleção atual, seja usando as teclas de direção ou clicando com o mouse.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-120">The user moves the current selection, either by using the arrow keys or by clicking the mouse.</span></span>
-   <span data-ttu-id="bf8c4-121">O usuário pressiona a tecla **delete** .</span><span class="sxs-lookup"><span data-stu-id="bf8c4-121">The user presses the **Delete** key.</span></span>
-   <span data-ttu-id="bf8c4-122">O usuário executa qualquer outra ação, como uma operação de colagem que não **envolve a** digitação.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-122">The user performs any other action, such as a paste operation that does **not** involve typing.</span></span>

<span data-ttu-id="bf8c4-123">Você pode enviar a mensagem em **\_ STOPGROUPTYPING** para interromper as ações de digitação consecutivas em grupos de desfazer menores.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-123">You can send the **EM\_STOPGROUPTYPING** message to break consecutive typing actions into smaller undo groups.</span></span> <span data-ttu-id="bf8c4-124">Por exemplo, você poderia enviar **em \_ STOPGROUPTYPING** depois de cada caractere ou de cada quebra de palavra.</span><span class="sxs-lookup"><span data-stu-id="bf8c4-124">For example, you could send **EM\_STOPGROUPTYPING** after each character or at each word break.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf8c4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf8c4-125">Requirements</span></span>



| <span data-ttu-id="bf8c4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf8c4-126">Requirement</span></span> | <span data-ttu-id="bf8c4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bf8c4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8c4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf8c4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bf8c4-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf8c4-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf8c4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf8c4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bf8c4-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf8c4-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf8c4-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf8c4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf8c4-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf8c4-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf8c4-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bf8c4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf8c4-135">**em \_ desfazer**</span><span class="sxs-lookup"><span data-stu-id="bf8c4-135">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





