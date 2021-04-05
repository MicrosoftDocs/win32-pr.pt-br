---
title: Mensagem de EM_GETCHARFORMAT (RichEdit. h)
description: Determina a formatação de caractere em um controle de edição rico.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- Controles de EM_GETCHARFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009452"
---
# <a name="em_getcharformat-message"></a><span data-ttu-id="37678-104">\_Mensagem em GETCHARFORMAT</span><span class="sxs-lookup"><span data-stu-id="37678-104">EM\_GETCHARFORMAT message</span></span>

<span data-ttu-id="37678-105">Determina a formatação de caractere em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="37678-105">Determines the character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="37678-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37678-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37678-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37678-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37678-108">Especifica o intervalo de texto do qual a formatação deve ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="37678-108">Specifies the range of text from which to retrieve formatting.</span></span> <span data-ttu-id="37678-109">Pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="37678-109">It can be one of the following values.</span></span>



| <span data-ttu-id="37678-110">Valor</span><span class="sxs-lookup"><span data-stu-id="37678-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="37678-111">Significado</span><span class="sxs-lookup"><span data-stu-id="37678-111">Meaning</span></span>                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="37678-112"><dt>**padrão de SCF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="37678-112"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="37678-113">A formatação de caractere padrão.</span><span class="sxs-lookup"><span data-stu-id="37678-113">The default character formatting.</span></span><br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="37678-114"><dt>**seleção de SCF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="37678-114"><dt>**SCF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="37678-115">A formatação de caractere da seleção atual.</span><span class="sxs-lookup"><span data-stu-id="37678-115">The current selection's character formatting.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37678-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37678-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37678-117">Uma estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) que recebe os atributos do primeiro caractere.</span><span class="sxs-lookup"><span data-stu-id="37678-117">A [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure that receives the attributes of the first character.</span></span> <span data-ttu-id="37678-118">O membro **dwMask** especifica quais atributos são consistentes em toda a seleção.</span><span class="sxs-lookup"><span data-stu-id="37678-118">The **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span> <span data-ttu-id="37678-119">Por exemplo, se toda a seleção estiver em itálico ou não em itálico, o CFM \_ itálico será definido; se a seleção estiver parcialmente em itálico e parcialmente não, o cfm \_ itálico não será definido.</span><span class="sxs-lookup"><span data-stu-id="37678-119">For example, if the entire selection is either in italics or not in italics, CFM\_ITALIC is set; if the selection is partly in italics and partly not, CFM\_ITALIC is not set.</span></span>

<span data-ttu-id="37678-120">Microsoft rich edit 2,0 e posterior: esse parâmetro pode ser um ponteiro para uma estrutura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , que é uma extensão da estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="37678-120">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="37678-121">Antes de enviar a mensagem em **\_ GETCHARFORMAT** , defina o membro **cbSize** da estrutura para indicar a versão da estrutura.</span><span class="sxs-lookup"><span data-stu-id="37678-121">Before sending the **EM\_GETCHARFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37678-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37678-122">Return value</span></span>

<span data-ttu-id="37678-123">Essa mensagem retorna o valor do membro **dwMask** da estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="37678-123">This message returns the value of the **dwMask** member of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="37678-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37678-124">Requirements</span></span>



| <span data-ttu-id="37678-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="37678-125">Requirement</span></span> | <span data-ttu-id="37678-126">Valor</span><span class="sxs-lookup"><span data-stu-id="37678-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37678-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37678-127">Minimum supported client</span></span><br/> | <span data-ttu-id="37678-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37678-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37678-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37678-129">Minimum supported server</span></span><br/> | <span data-ttu-id="37678-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37678-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37678-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37678-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="37678-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="37678-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37678-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="37678-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="37678-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="37678-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="37678-135">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="37678-135">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="37678-136">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="37678-136">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





