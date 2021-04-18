---
title: Mensagem de EM_SETSCROLLPOS (RichEdit. h)
description: Rola o conteúdo de um controle de edição rico para o ponto especificado.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- Controles de EM_SETSCROLLPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455760"
---
# <a name="em_setscrollpos-message"></a><span data-ttu-id="d9419-104">\_Mensagem em SETSCROLLPOS</span><span class="sxs-lookup"><span data-stu-id="d9419-104">EM\_SETSCROLLPOS message</span></span>

<span data-ttu-id="d9419-105">Rola o conteúdo de um controle de edição rico para o ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="d9419-105">Scrolls the contents of a rich edit control to the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9419-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9419-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9419-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9419-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9419-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d9419-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d9419-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9419-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9419-110">Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que especifica um ponto no espaço de texto virtual do documento, expresso em pixels.</span><span class="sxs-lookup"><span data-stu-id="d9419-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure which specifies a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="d9419-111">O documento será rolado até que esse ponto esteja localizado no canto superior esquerdo da janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="d9419-111">The document will be scrolled until this point is located in the upper-left corner of the edit control window.</span></span> <span data-ttu-id="d9419-112">Se você quiser alterar a exibição de modo que o canto superior esquerdo da exibição tenha duas linhas abaixo e um caractere na borda esquerda.</span><span class="sxs-lookup"><span data-stu-id="d9419-112">If you want to change the view such that the upper left corner of the view is two lines down and one character in from the left edge.</span></span> <span data-ttu-id="d9419-113">Você passaria um ponto de (7, 22).</span><span class="sxs-lookup"><span data-stu-id="d9419-113">You would pass a point of (7, 22).</span></span>

<span data-ttu-id="d9419-114">O controle Rich Edit Verifica as coordenadas x e y e as ajusta, se necessário, para que uma linha completa seja exibida na parte superior.</span><span class="sxs-lookup"><span data-stu-id="d9419-114">The rich edit control checks the x and y coordinates and adjusts them if necessary, so that a complete line is displayed at the top.</span></span> <span data-ttu-id="d9419-115">Ele também garante que o texto nunca seja completamente rolado para fora do retângulo de exibição.</span><span class="sxs-lookup"><span data-stu-id="d9419-115">It also ensures that the text is never completely scrolled off the view rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9419-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9419-116">Return value</span></span>

<span data-ttu-id="d9419-117">Essa mensagem sempre retorna 1.</span><span class="sxs-lookup"><span data-stu-id="d9419-117">This message always returns 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9419-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9419-118">Requirements</span></span>



| <span data-ttu-id="d9419-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9419-119">Requirement</span></span> | <span data-ttu-id="d9419-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d9419-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9419-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9419-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9419-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9419-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9419-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9419-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9419-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9419-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9419-125">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d9419-125">Redistributable</span></span><br/>          | <span data-ttu-id="d9419-126">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="d9419-126">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="d9419-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9419-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9419-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9419-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9419-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9419-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9419-130">**em \_ GETSCROLLPOS**</span><span class="sxs-lookup"><span data-stu-id="d9419-130">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> </dl>

 

