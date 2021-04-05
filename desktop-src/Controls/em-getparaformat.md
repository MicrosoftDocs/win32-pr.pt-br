---
title: Mensagem de EM_GETPARAFORMAT (RichEdit. h)
description: Recupera a formatação de parágrafo da seleção atual em um controle de edição rico.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- Controles de EM_GETPARAFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918986"
---
# <a name="em_getparaformat-message"></a><span data-ttu-id="efe3d-104">\_Mensagem em GETPARAFORMAT</span><span class="sxs-lookup"><span data-stu-id="efe3d-104">EM\_GETPARAFORMAT message</span></span>

<span data-ttu-id="efe3d-105">Recupera a formatação de parágrafo da seleção atual em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="efe3d-105">Retrieves the paragraph formatting of the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="efe3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efe3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe3d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="efe3d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efe3d-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="efe3d-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="efe3d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efe3d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efe3d-110">Ponteiro para uma estrutura [**PARAformativa**](/windows/desktop/api/Richedit/ns-richedit-paraformat) que recebe os atributos de formatação de parágrafo da seleção atual.</span><span class="sxs-lookup"><span data-stu-id="efe3d-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure that receives the paragraph formatting attributes of the current selection.</span></span>

<span data-ttu-id="efe3d-111">Se mais de um parágrafo for selecionado, a estrutura receberá os atributos do primeiro parágrafo e o membro **dwMask** especificará quais atributos são consistentes em toda a seleção.</span><span class="sxs-lookup"><span data-stu-id="efe3d-111">If more than one paragraph is selected, the structure receives the attributes of the first paragraph, and the **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span>

<span data-ttu-id="efe3d-112">Microsoft rich edit 2,0 e posterior: esse parâmetro pode ser um ponteiro para uma estrutura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , que é uma extensão da estrutura [**paraformativa**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="efe3d-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="efe3d-113">Antes de enviar a mensagem em **\_ GETPARAFORMAT** , defina o membro **cbSize** da estrutura para indicar a versão da estrutura.</span><span class="sxs-lookup"><span data-stu-id="efe3d-113">Before sending the **EM\_GETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe3d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efe3d-114">Return value</span></span>

<span data-ttu-id="efe3d-115">Essa mensagem retorna o valor do membro **dwMask** da estrutura [**paraformate**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="efe3d-115">This message returns the value of the **dwMask** member of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe3d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efe3d-116">Requirements</span></span>



| <span data-ttu-id="efe3d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="efe3d-117">Requirement</span></span> | <span data-ttu-id="efe3d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="efe3d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efe3d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efe3d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="efe3d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efe3d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="efe3d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efe3d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="efe3d-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efe3d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efe3d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="efe3d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="efe3d-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="efe3d-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efe3d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="efe3d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="efe3d-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="efe3d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="efe3d-127">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="efe3d-127">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="efe3d-128">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="efe3d-128">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





