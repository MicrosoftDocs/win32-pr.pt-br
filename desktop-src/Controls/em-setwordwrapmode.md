---
title: Mensagem de EM_SETWORDWRAPMODE (RichEdit. h)
description: Define as opções de quebra automática de palavras e quebra de palavras para um controle de edição rico.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- Controles de EM_SETWORDWRAPMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009481"
---
# <a name="em_setwordwrapmode-message"></a><span data-ttu-id="1056c-104">\_Mensagem em SETwordwrapmode</span><span class="sxs-lookup"><span data-stu-id="1056c-104">EM\_SETWORDWRAPMODE message</span></span>

<span data-ttu-id="1056c-105">Define as opções de quebra automática de palavras e quebra de palavras para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="1056c-105">Sets the word-wrapping and word-breaking options for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="1056c-106">Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="1056c-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="1056c-107">Não há suporte para ele em nenhuma versão posterior.</span><span class="sxs-lookup"><span data-stu-id="1056c-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="1056c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1056c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1056c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1056c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1056c-110">Especifica um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1056c-110">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="1056c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1056c-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="1056c-112">Significado</span><span class="sxs-lookup"><span data-stu-id="1056c-112">Meaning</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <span data-ttu-id="1056c-113"><dt>**WBF \_ WORDWRAP**</dt></span><span class="sxs-lookup"><span data-stu-id="1056c-113"><dt>**WBF\_WORDWRAP**</dt></span></span> </dl>    | <span data-ttu-id="1056c-114">Permite operações de quebra automática de palavras específicas do idioma, como kinsoku em Japonês.</span><span class="sxs-lookup"><span data-stu-id="1056c-114">Enables Asian-specific word wrap operations, such as kinsoku in Japanese.</span></span> <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <span data-ttu-id="1056c-115"><dt>**WBF \_ justificação**</dt></span><span class="sxs-lookup"><span data-stu-id="1056c-115"><dt>**WBF\_WORDBREAK**</dt></span></span> </dl> | <span data-ttu-id="1056c-116">Habilita as operações de separação de palavras em inglês em Japonês e chinês.</span><span class="sxs-lookup"><span data-stu-id="1056c-116">Enables English word-breaking operations in Japanese and Chinese.</span></span> <span data-ttu-id="1056c-117">Habilita a operação de quebra de palavras hangeul.</span><span class="sxs-lookup"><span data-stu-id="1056c-117">Enables Hangeul word-breaking operation.</span></span><br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <span data-ttu-id="1056c-118"><dt>**estouro de WBF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1056c-118"><dt>**WBF\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="1056c-119">Reconhece Pontuação de estouro.</span><span class="sxs-lookup"><span data-stu-id="1056c-119">Recognizes overflow punctuation.</span></span> <span data-ttu-id="1056c-120">(Não tem suporte no momento.)</span><span class="sxs-lookup"><span data-stu-id="1056c-120">(Not currently supported.)</span></span><br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <span data-ttu-id="1056c-121"><dt>**WBF \_ LEVEL1**</dt></span><span class="sxs-lookup"><span data-stu-id="1056c-121"><dt>**WBF\_LEVEL1**</dt></span></span> </dl>          | <span data-ttu-id="1056c-122">Define a tabela de Pontuação de nível 1 como padrão.</span><span class="sxs-lookup"><span data-stu-id="1056c-122">Sets the Level 1 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <span data-ttu-id="1056c-123"><dt>**WBF \_ LEVEL2**</dt></span><span class="sxs-lookup"><span data-stu-id="1056c-123"><dt>**WBF\_LEVEL2**</dt></span></span> </dl>          | <span data-ttu-id="1056c-124">Define a tabela de Pontuação de nível 2 como o padrão.</span><span class="sxs-lookup"><span data-stu-id="1056c-124">Sets the Level 2 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <span data-ttu-id="1056c-125"><dt>**WBF \_ personalizado**</dt></span><span class="sxs-lookup"><span data-stu-id="1056c-125"><dt>**WBF\_CUSTOM**</dt></span></span> </dl>          | <span data-ttu-id="1056c-126">Define a tabela de pontuação definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1056c-126">Sets the application-defined punctuation table.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="1056c-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1056c-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1056c-128">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1056c-128">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1056c-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1056c-129">Return value</span></span>

<span data-ttu-id="1056c-130">Essa mensagem retorna as opções de quebra automática de texto e quebra de palavra atuais.</span><span class="sxs-lookup"><span data-stu-id="1056c-130">This message returns the current word-wrapping and word-breaking options.</span></span>

## <a name="remarks"></a><span data-ttu-id="1056c-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="1056c-131">Remarks</span></span>

<span data-ttu-id="1056c-132">Esta mensagem não deve ser enviada pelo procedimento de quebra de palavras definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1056c-132">This message must not be sent by the application defined word breaking procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1056c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1056c-133">Requirements</span></span>



| <span data-ttu-id="1056c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1056c-134">Requirement</span></span> | <span data-ttu-id="1056c-135">Valor</span><span class="sxs-lookup"><span data-stu-id="1056c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1056c-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1056c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1056c-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1056c-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1056c-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1056c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1056c-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1056c-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1056c-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1056c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1056c-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1056c-141"><dt>Richedit.h</dt></span></span> </dl> |



 

 





