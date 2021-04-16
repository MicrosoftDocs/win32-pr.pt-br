---
title: Mensagem de EM_GETSCROLLPOS (RichEdit. h)
description: Obtém a posição de rolagem atual do controle de edição.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- Controles de EM_GETSCROLLPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455069"
---
# <a name="em_getscrollpos-message"></a><span data-ttu-id="2872d-104">\_Mensagem em GETSCROLLPOS</span><span class="sxs-lookup"><span data-stu-id="2872d-104">EM\_GETSCROLLPOS message</span></span>

<span data-ttu-id="2872d-105">Obtém a posição de rolagem atual do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="2872d-105">Obtains the current scroll position of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2872d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2872d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2872d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2872d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2872d-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2872d-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2872d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2872d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2872d-110">Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2872d-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="2872d-111">Depois de chamar em **\_ GETSCROLLPOS**, esses parâmetros contêm um ponto no espaço de texto virtual do documento, expresso em pixels.</span><span class="sxs-lookup"><span data-stu-id="2872d-111">After calling **EM\_GETSCROLLPOS**, this parameters contains a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="2872d-112">Esse ponto será o ponto localizado atualmente no canto superior esquerdo da janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="2872d-112">This point will be the point that is currently located in the upper-left corner of the edit control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2872d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2872d-113">Return value</span></span>

<span data-ttu-id="2872d-114">Essa mensagem sempre retorna 1.</span><span class="sxs-lookup"><span data-stu-id="2872d-114">This message always returns 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="2872d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2872d-115">Remarks</span></span>

<span data-ttu-id="2872d-116">Os valores retornados na estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) são valores de 16 bits (mesmo nos campos de largura de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="2872d-116">The values returned in the [**POINT**](/previous-versions//dd162805(v=vs.85)) structure are 16-bit values (even in the 32-bit wide fields).</span></span>

## <a name="requirements"></a><span data-ttu-id="2872d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2872d-117">Requirements</span></span>



| <span data-ttu-id="2872d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2872d-118">Requirement</span></span> | <span data-ttu-id="2872d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2872d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2872d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2872d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2872d-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2872d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2872d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2872d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2872d-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2872d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2872d-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2872d-124">Redistributable</span></span><br/>          | <span data-ttu-id="2872d-125">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="2872d-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="2872d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2872d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2872d-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2872d-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2872d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2872d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2872d-129">**em \_ SETSCROLLPOS**</span><span class="sxs-lookup"><span data-stu-id="2872d-129">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

