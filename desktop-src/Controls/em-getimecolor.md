---
title: Mensagem de EM_GETIMECOLOR (RichEdit. h)
description: Recupera a cor de composição do IME (editor de método de entrada).
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- Controles de EM_GETIMECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a19061651787ff94575f8bc64a69f06d445a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918807"
---
# <a name="em_getimecolor-message"></a><span data-ttu-id="bdc10-104">\_Mensagem em GETIMECOLOR</span><span class="sxs-lookup"><span data-stu-id="bdc10-104">EM\_GETIMECOLOR message</span></span>

<span data-ttu-id="bdc10-105">Recupera a cor de composição do IME (editor de método de entrada).</span><span class="sxs-lookup"><span data-stu-id="bdc10-105">Retrieves the Input Method Editor (IME) composition color.</span></span>

> [!Note]  
> <span data-ttu-id="bdc10-106">Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="bdc10-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="bdc10-107">Não há suporte para ele em versões posteriores do rich edit.</span><span class="sxs-lookup"><span data-stu-id="bdc10-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="bdc10-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdc10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc10-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdc10-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc10-110">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bdc10-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bdc10-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdc10-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc10-112">Uma matriz de quatro elementos de estruturas [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) que recebe a cor de composição.</span><span class="sxs-lookup"><span data-stu-id="bdc10-112">A four-element array of [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structures that receives the composition color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc10-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdc10-113">Return value</span></span>

<span data-ttu-id="bdc10-114">Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="bdc10-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bdc10-115">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="bdc10-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc10-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdc10-116">Requirements</span></span>



| <span data-ttu-id="bdc10-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdc10-117">Requirement</span></span> | <span data-ttu-id="bdc10-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bdc10-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc10-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdc10-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc10-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bdc10-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdc10-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdc10-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc10-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bdc10-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdc10-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdc10-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc10-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc10-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc10-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdc10-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc10-126">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="bdc10-126">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





