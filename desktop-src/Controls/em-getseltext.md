---
title: Mensagem de EM_GETSELTEXT (RichEdit. h)
description: Recupera o texto atualmente selecionado em um controle de edição rico.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- Controles de EM_GETSELTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824365"
---
# <a name="em_getseltext-message"></a><span data-ttu-id="d2770-104">\_Mensagem em GETSELTEXT</span><span class="sxs-lookup"><span data-stu-id="d2770-104">EM\_GETSELTEXT message</span></span>

<span data-ttu-id="d2770-105">Recupera o texto atualmente selecionado em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="d2770-105">Retrieves the currently selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2770-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2770-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2770-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2770-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2770-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d2770-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2770-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2770-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2770-110">Ponteiro para um buffer que recebe o texto selecionado.</span><span class="sxs-lookup"><span data-stu-id="d2770-110">Pointer to a buffer that receives the selected text.</span></span> <span data-ttu-id="d2770-111">O aplicativo de chamada deve garantir que o buffer seja grande o suficiente para manter o texto selecionado.</span><span class="sxs-lookup"><span data-stu-id="d2770-111">The calling application must ensure that the buffer is large enough to hold the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2770-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2770-112">Return value</span></span>

<span data-ttu-id="d2770-113">Essa mensagem retorna o número de caracteres copiados, não incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="d2770-113">This message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2770-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2770-114">Requirements</span></span>



| <span data-ttu-id="d2770-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2770-115">Requirement</span></span> | <span data-ttu-id="d2770-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d2770-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2770-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2770-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d2770-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2770-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2770-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2770-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d2770-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2770-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2770-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2770-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2770-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2770-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





