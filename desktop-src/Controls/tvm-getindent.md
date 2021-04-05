---
title: Mensagem de TVM_GETINDENT (commctrl. h)
description: Recupera o valor, em pixels, que os itens filho são recuados em relação aos seus itens pai. Você pode enviar essa mensagem explicitamente ou usando a macro do TreeView \_ GetIndent.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- Controles de TVM_GETINDENT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824747"
---
# <a name="tvm_getindent-message"></a><span data-ttu-id="f018e-105">TVM \_ GETrecuo de mensagem</span><span class="sxs-lookup"><span data-stu-id="f018e-105">TVM\_GETINDENT message</span></span>

<span data-ttu-id="f018e-106">Recupera o valor, em pixels, que os itens filho são recuados em relação aos seus itens pai.</span><span class="sxs-lookup"><span data-stu-id="f018e-106">Retrieves the amount, in pixels, that child items are indented relative to their parent items.</span></span> <span data-ttu-id="f018e-107">Você pode enviar essa mensagem explicitamente ou usando a macro do [**TreeView \_ GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .</span><span class="sxs-lookup"><span data-stu-id="f018e-107">You can send this message explicitly or by using the [**TreeView\_GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f018e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f018e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f018e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f018e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f018e-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f018e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f018e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f018e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f018e-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f018e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f018e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f018e-113">Return value</span></span>

<span data-ttu-id="f018e-114">Retorna a quantidade de recuo.</span><span class="sxs-lookup"><span data-stu-id="f018e-114">Returns the amount of indentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f018e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f018e-115">Requirements</span></span>



| <span data-ttu-id="f018e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f018e-116">Requirement</span></span> | <span data-ttu-id="f018e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f018e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f018e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f018e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f018e-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f018e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f018e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f018e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f018e-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f018e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f018e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f018e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f018e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f018e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





