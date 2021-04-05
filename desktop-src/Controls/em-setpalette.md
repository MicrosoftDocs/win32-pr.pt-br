---
title: Mensagem de EM_SETPALETTE (RichEdit. h)
description: Altera a paleta que um controle de edição avançado usa para sua janela de exibição.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- Controles de EM_SETPALETTE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009268"
---
# <a name="em_setpalette-message"></a><span data-ttu-id="9116d-104">\_Mensagem em SETpalette</span><span class="sxs-lookup"><span data-stu-id="9116d-104">EM\_SETPALETTE message</span></span>

<span data-ttu-id="9116d-105">Altera a paleta que um controle de edição avançado usa para sua janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="9116d-105">Changes the palette that a rich edit control uses for its display window.</span></span>

## <a name="parameters"></a><span data-ttu-id="9116d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9116d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9116d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9116d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9116d-108">Identificador para a nova paleta usada pelo controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="9116d-108">Handle to the new palette used by the rich edit control.</span></span>

</dd> <dt>

<span data-ttu-id="9116d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9116d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9116d-110">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9116d-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9116d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9116d-111">Return value</span></span>

<span data-ttu-id="9116d-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9116d-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9116d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9116d-113">Remarks</span></span>

<span data-ttu-id="9116d-114">O controle de edição rico não verifica se a nova paleta é válida.</span><span class="sxs-lookup"><span data-stu-id="9116d-114">The rich edit control does not check whether the new palette is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="9116d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9116d-115">Requirements</span></span>



| <span data-ttu-id="9116d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9116d-116">Requirement</span></span> | <span data-ttu-id="9116d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9116d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9116d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9116d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9116d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9116d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9116d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9116d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9116d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9116d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9116d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9116d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9116d-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9116d-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





