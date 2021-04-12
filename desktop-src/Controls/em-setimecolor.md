---
title: Mensagem de EM_SETIMECOLOR (RichEdit. h)
description: Define a cor de composição do IME (editor de método de entrada) para um controle de edição rico.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- Controles de EM_SETIMECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455348"
---
# <a name="em_setimecolor-message"></a><span data-ttu-id="7f416-104">\_Mensagem em SETIMECOLOR</span><span class="sxs-lookup"><span data-stu-id="7f416-104">EM\_SETIMECOLOR message</span></span>

<span data-ttu-id="7f416-105">Define a cor de composição do IME (editor de método de entrada) para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="7f416-105">Sets the Input Method Editor (IME) composition color for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="7f416-106">Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="7f416-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="7f416-107">Não há suporte para ele em nenhuma versão posterior.</span><span class="sxs-lookup"><span data-stu-id="7f416-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="7f416-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f416-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f416-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f416-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f416-110">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7f416-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7f416-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f416-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f416-112">Ponteiro para uma estrutura [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) que contém a cor de composição a ser definida.</span><span class="sxs-lookup"><span data-stu-id="7f416-112">Pointer to a [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structure that contains the composition color to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f416-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f416-113">Return value</span></span>

<span data-ttu-id="7f416-114">Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7f416-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="7f416-115">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="7f416-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f416-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f416-116">Requirements</span></span>



| <span data-ttu-id="7f416-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f416-117">Requirement</span></span> | <span data-ttu-id="7f416-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7f416-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f416-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f416-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f416-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f416-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f416-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f416-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f416-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f416-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f416-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f416-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f416-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f416-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f416-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f416-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="7f416-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7f416-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7f416-127">**em \_ GETIMECOLOR**</span><span class="sxs-lookup"><span data-stu-id="7f416-127">**EM\_GETIMECOLOR**</span></span>](em-getimecolor.md)
</dt> <dt>

[<span data-ttu-id="7f416-128">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="7f416-128">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





