---
title: Mensagem de EM_GETWORDWRAPMODE (RichEdit. h)
description: Obtém as opções de quebra automática de palavra e de quebra de palavras para o controle de edição rico.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- Controles de EM_GETWORDWRAPMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454763"
---
# <a name="em_getwordwrapmode-message"></a><span data-ttu-id="0c177-104">\_Mensagem em GETwordwrapmode</span><span class="sxs-lookup"><span data-stu-id="0c177-104">EM\_GETWORDWRAPMODE message</span></span>

<span data-ttu-id="0c177-105">Obtém as opções de quebra automática de palavra e de quebra de palavras para o controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="0c177-105">Gets the current word wrap and word-break options for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="0c177-106">Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="0c177-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="0c177-107">Não há suporte para ele em versões posteriores do rich edit.</span><span class="sxs-lookup"><span data-stu-id="0c177-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="0c177-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c177-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c177-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c177-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c177-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0c177-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0c177-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c177-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c177-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0c177-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c177-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c177-113">Return value</span></span>

<span data-ttu-id="0c177-114">A mensagem retorna as opções de quebra automática de texto e de quebra de palavra atual.</span><span class="sxs-lookup"><span data-stu-id="0c177-114">The message returns the current word wrap and word-break options.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c177-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c177-115">Remarks</span></span>

<span data-ttu-id="0c177-116">Essa mensagem não deve ser enviada pelo procedimento de quebra de palavra definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c177-116">This message must not be sent by the application-defined, word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c177-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c177-117">Requirements</span></span>



| <span data-ttu-id="0c177-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c177-118">Requirement</span></span> | <span data-ttu-id="0c177-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0c177-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c177-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c177-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0c177-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c177-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c177-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c177-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0c177-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c177-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c177-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c177-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c177-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c177-125"><dt>Richedit.h</dt></span></span> </dl> |



 

 





