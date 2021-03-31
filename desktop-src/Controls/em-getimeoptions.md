---
title: Mensagem de EM_GETIMEOPTIONS (RichEdit. h)
description: Recupera as opções atuais do IME (editor de método de entrada).
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- Controles de EM_GETIMEOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085936"
---
# <a name="em_getimeoptions-message"></a><span data-ttu-id="7c26d-104">\_Mensagem em GETIMEOPTIONS</span><span class="sxs-lookup"><span data-stu-id="7c26d-104">EM\_GETIMEOPTIONS message</span></span>

<span data-ttu-id="7c26d-105">Recupera as opções atuais do IME (editor de método de entrada).</span><span class="sxs-lookup"><span data-stu-id="7c26d-105">Retrieves the current Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="7c26d-106">Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="7c26d-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="7c26d-107">Não há suporte para ele em versões posteriores do rich edit.</span><span class="sxs-lookup"><span data-stu-id="7c26d-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="7c26d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c26d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c26d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c26d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c26d-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7c26d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7c26d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c26d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c26d-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7c26d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c26d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c26d-113">Return value</span></span>

<span data-ttu-id="7c26d-114">Essa mensagem retorna um ou mais dos valores de sinalizador de opção do IME descritos na mensagem em [**\_ SETIMEOPTIONS**](em-setimeoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="7c26d-114">This message returns one or more of the IME option flag values described in the [**EM\_SETIMEOPTIONS**](em-setimeoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c26d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c26d-115">Requirements</span></span>



| <span data-ttu-id="7c26d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c26d-116">Requirement</span></span> | <span data-ttu-id="7c26d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7c26d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c26d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c26d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7c26d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c26d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c26d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c26d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7c26d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c26d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c26d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c26d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c26d-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c26d-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c26d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c26d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c26d-125">**em \_ SETIMEOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="7c26d-125">**EM\_SETIMEOPTIONS**</span></span>](em-setimeoptions.md)
</dt> </dl>

 

 





