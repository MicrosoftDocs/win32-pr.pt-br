---
title: Mensagem de EM_SETPUNCTUATION (RichEdit. h)
description: Define os caracteres de Pontuação para um controle de edição rico.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- Controles de EM_SETPUNCTUATION de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086185"
---
# <a name="em_setpunctuation-message"></a><span data-ttu-id="811d1-104">\_Mensagem em SETpontuation</span><span class="sxs-lookup"><span data-stu-id="811d1-104">EM\_SETPUNCTUATION message</span></span>

<span data-ttu-id="811d1-105">Define os caracteres de Pontuação para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="811d1-105">Sets the punctuation characters for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="811d1-106">Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="811d1-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="811d1-107">Não há suporte para ele em nenhuma versão posterior.</span><span class="sxs-lookup"><span data-stu-id="811d1-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="811d1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="811d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="811d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="811d1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="811d1-110">Especifica o tipo de pontuação, que pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="811d1-110">Specifies the punctuation type, which can be one of the following values.</span></span>



| <span data-ttu-id="811d1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="811d1-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="811d1-112">Significado</span><span class="sxs-lookup"><span data-stu-id="811d1-112">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="811d1-113"><dt>**líder do PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="811d1-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="811d1-114">Caracteres de Pontuação à esquerda.</span><span class="sxs-lookup"><span data-stu-id="811d1-114">Leading punctuation characters.</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="811d1-115"><dt>**PC a \_ seguir**</dt></span><span class="sxs-lookup"><span data-stu-id="811d1-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="811d1-116">Caracteres de Pontuação a seguir.</span><span class="sxs-lookup"><span data-stu-id="811d1-116">Following punctuation characters.</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="811d1-117"><dt>**delimitador de PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="811d1-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="811d1-118">Delimitador.</span><span class="sxs-lookup"><span data-stu-id="811d1-118">Delimiter.</span></span><br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <span data-ttu-id="811d1-119"><dt>**PC \_ ESTOURO**</dt></span><span class="sxs-lookup"><span data-stu-id="811d1-119"><dt>**PC\_OVERFLOW** </dt></span></span> </dl> | <span data-ttu-id="811d1-120">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="811d1-120">Not supported.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="811d1-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="811d1-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="811d1-122">Ponteiro para uma estrutura de [**Pontuação**](/windows/desktop/api/Richedit/ns-richedit-punctuation) que contém os caracteres de pontuação.</span><span class="sxs-lookup"><span data-stu-id="811d1-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that contains the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="811d1-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="811d1-123">Return value</span></span>

<span data-ttu-id="811d1-124">Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="811d1-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="811d1-125">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="811d1-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="811d1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="811d1-126">Requirements</span></span>



| <span data-ttu-id="811d1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="811d1-127">Requirement</span></span> | <span data-ttu-id="811d1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="811d1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="811d1-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="811d1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="811d1-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="811d1-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="811d1-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="811d1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="811d1-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="811d1-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="811d1-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="811d1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="811d1-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="811d1-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="811d1-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="811d1-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="811d1-136">**Referência**</span><span class="sxs-lookup"><span data-stu-id="811d1-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="811d1-137">**em \_ GETpontuation**</span><span class="sxs-lookup"><span data-stu-id="811d1-137">**EM\_GETPUNCTUATION**</span></span>](em-getpunctuation.md)
</dt> <dt>

[<span data-ttu-id="811d1-138">**Pontuação**</span><span class="sxs-lookup"><span data-stu-id="811d1-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





