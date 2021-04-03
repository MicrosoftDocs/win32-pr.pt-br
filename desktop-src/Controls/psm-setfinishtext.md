---
title: Mensagem de PSM_SETFINISHTEXT (Prsht. h)
description: Define o texto do botão concluir em um assistente, mostra e habilita o botão e oculta os botões Avançar e voltar. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- Controles de PSM_SETFINISHTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644299"
---
# <a name="psm_setfinishtext-message"></a><span data-ttu-id="4c3b0-105">Mensagem de PSM \_ SETFINISHTEXT</span><span class="sxs-lookup"><span data-stu-id="4c3b0-105">PSM\_SETFINISHTEXT message</span></span>

<span data-ttu-id="4c3b0-106">Define o texto do botão **concluir** em um assistente, mostra e habilita o botão e oculta os botões **Avançar** e **voltar** .</span><span class="sxs-lookup"><span data-stu-id="4c3b0-106">Sets the text of the **Finish** button in a wizard, shows and enables the button, and hides the **Next** and **Back** buttons.</span></span> <span data-ttu-id="4c3b0-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .</span><span class="sxs-lookup"><span data-stu-id="4c3b0-107">You can send this message explicitly or by using the [**PropSheet\_SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c3b0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c3b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c3b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c3b0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c3b0-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4c3b0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4c3b0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c3b0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c3b0-112">Ponteiro para o novo texto do botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="4c3b0-112">Pointer to the new text for the **Finish** button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c3b0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c3b0-113">Return value</span></span>

<span data-ttu-id="4c3b0-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4c3b0-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c3b0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c3b0-115">Remarks</span></span>

<span data-ttu-id="4c3b0-116">Por padrão, o botão **concluir** não tem um acelerador de teclado.</span><span class="sxs-lookup"><span data-stu-id="4c3b0-116">By default, the **Finish** button does not have a keyboard accelerator.</span></span> <span data-ttu-id="4c3b0-117">Você pode criar um acelerador de teclado com essa mensagem incluindo um e comercial (&) na cadeia de texto que você atribui ao *lParam*.</span><span class="sxs-lookup"><span data-stu-id="4c3b0-117">You can create a keyboard accelerator with this message by including an ampersand (&) in the text string that you assign to *lParam*.</span></span> <span data-ttu-id="4c3b0-118">Por exemplo, "&concluir" define F como a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="4c3b0-118">For example, "&Finish" defines F as the accelerator key.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c3b0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c3b0-119">Requirements</span></span>



| <span data-ttu-id="4c3b0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c3b0-120">Requirement</span></span> | <span data-ttu-id="4c3b0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4c3b0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3b0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c3b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4c3b0-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c3b0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4c3b0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c3b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4c3b0-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c3b0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4c3b0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c3b0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c3b0-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c3b0-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="4c3b0-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4c3b0-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4c3b0-129">**PSM \_ SETFINISHTEXTW** (Unicode) e **PSM \_ SETFINISHTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4c3b0-129">**PSM\_SETFINISHTEXTW** (Unicode) and **PSM\_SETFINISHTEXTA** (ANSI)</span></span><br/>    |



 

 





