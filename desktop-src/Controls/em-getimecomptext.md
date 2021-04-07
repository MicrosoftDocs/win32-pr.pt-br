---
title: Mensagem de EM_GETIMECOMPTEXT (RichEdit. h)
description: Recupera o texto de composição do IME (editor de método de entrada).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- Controles de EM_GETIMECOMPTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918806"
---
# <a name="em_getimecomptext-message"></a><span data-ttu-id="9958c-104">\_Mensagem em GETIMECOMPTEXT</span><span class="sxs-lookup"><span data-stu-id="9958c-104">EM\_GETIMECOMPTEXT message</span></span>

<span data-ttu-id="9958c-105">Recupera o texto de composição do IME (editor de método de entrada).</span><span class="sxs-lookup"><span data-stu-id="9958c-105">Retrieves the Input Method Editor (IME) composition text.</span></span>

## <a name="parameters"></a><span data-ttu-id="9958c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9958c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9958c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9958c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9958c-108">A estrutura [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) .</span><span class="sxs-lookup"><span data-stu-id="9958c-108">The [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9958c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9958c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9958c-110">O buffer que recebe o texto de composição.</span><span class="sxs-lookup"><span data-stu-id="9958c-110">The buffer that receives the composition text.</span></span> <span data-ttu-id="9958c-111">O tamanho desse buffer está contido no membro **CB** da estrutura *wParam* .</span><span class="sxs-lookup"><span data-stu-id="9958c-111">The size of this buffer is contained in the **cb** member of the *wParam* structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9958c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9958c-112">Return value</span></span>

<span data-ttu-id="9958c-113">Se for bem-sucedido, o valor de retorno será o número de caracteres Unicode copiados para o buffer.</span><span class="sxs-lookup"><span data-stu-id="9958c-113">If successful, the return value is the number of Unicode characters copied to the buffer.</span></span> <span data-ttu-id="9958c-114">Caso contrário, será zero.</span><span class="sxs-lookup"><span data-stu-id="9958c-114">Otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9958c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9958c-115">Remarks</span></span>

<span data-ttu-id="9958c-116">Essa mensagem usa apenas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="9958c-116">This message only takes Unicode strings.</span></span>

<span data-ttu-id="9958c-117">**Aviso de segurança:** Certifique-se de ter um buffer suficiente para o tamanho da entrada.</span><span class="sxs-lookup"><span data-stu-id="9958c-117">**Security Warning:** Be sure to have a buffer sufficient for the size of the input.</span></span> <span data-ttu-id="9958c-118">A falha em fazer isso pode causar problemas para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9958c-118">Failure to do so could cause problems for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="9958c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9958c-119">Requirements</span></span>



| <span data-ttu-id="9958c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9958c-120">Requirement</span></span> | <span data-ttu-id="9958c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9958c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9958c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9958c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9958c-123">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="9958c-123">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9958c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9958c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9958c-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9958c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9958c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9958c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9958c-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9958c-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9958c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9958c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9958c-129">**IMECOMPTEXT**</span><span class="sxs-lookup"><span data-stu-id="9958c-129">**IMECOMPTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





