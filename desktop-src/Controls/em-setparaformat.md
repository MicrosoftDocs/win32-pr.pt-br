---
title: Mensagem de EM_SETPARAFORMAT (RichEdit. h)
description: Define a formatação de parágrafo para a seleção atual em um controle de edição rico.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- Controles de EM_SETPARAFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455020"
---
# <a name="em_setparaformat-message"></a><span data-ttu-id="d5cf3-104">\_Mensagem em SETPARAFORMAT</span><span class="sxs-lookup"><span data-stu-id="d5cf3-104">EM\_SETPARAFORMAT message</span></span>

<span data-ttu-id="d5cf3-105">Define a formatação de parágrafo para a seleção atual em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-105">Sets the paragraph formatting for the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5cf3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5cf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5cf3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5cf3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5cf3-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d5cf3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5cf3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5cf3-110">Ponteiro para uma estrutura [**PARAformativa**](/windows/desktop/api/Richedit/ns-richedit-paraformat) especificando os novos atributos de formatação de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure specifying the new paragraph formatting attributes.</span></span> <span data-ttu-id="d5cf3-111">Somente os atributos especificados pelo membro **dwMask** são alterados.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-111">Only the attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="d5cf3-112">Microsoft rich edit 2,0 e posterior: esse parâmetro pode ser um ponteiro para uma estrutura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , que é uma extensão da estrutura [**paraformativa**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="d5cf3-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="d5cf3-113">Antes de enviar a mensagem em **\_ SETPARAFORMAT** , defina o membro **cbSize** da estrutura para indicar a versão da estrutura.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-113">Before sending the **EM\_SETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5cf3-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5cf3-114">Return value</span></span>

<span data-ttu-id="d5cf3-115">Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-115">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d5cf3-116">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5cf3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5cf3-117">Requirements</span></span>



| <span data-ttu-id="d5cf3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5cf3-118">Requirement</span></span> | <span data-ttu-id="d5cf3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d5cf3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5cf3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5cf3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5cf3-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5cf3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5cf3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5cf3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5cf3-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5cf3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5cf3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5cf3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5cf3-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5cf3-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5cf3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5cf3-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5cf3-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d5cf3-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d5cf3-128">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d5cf3-128">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="d5cf3-129">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="d5cf3-129">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





