---
title: Mensagem de SB_SIMPLE (commctrl. h)
description: Especifica se uma janela de status exibe texto simples ou exibe todas as partes da janela definidas por uma mensagem do SB \_ SETparts anterior.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- Controles de SB_SIMPLE de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086017"
---
# <a name="sb_simple-message"></a><span data-ttu-id="e31b9-104">\_Mensagem simples do SB</span><span class="sxs-lookup"><span data-stu-id="e31b9-104">SB\_SIMPLE message</span></span>

<span data-ttu-id="e31b9-105">Especifica se uma janela de status exibe texto simples ou exibe todas as partes da janela definidas por uma mensagem do [**SB \_ SetParts**](sb-setparts.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="e31b9-105">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="e31b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e31b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e31b9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e31b9-108">Sinalizador de tipo de exibição.</span><span class="sxs-lookup"><span data-stu-id="e31b9-108">Display type flag.</span></span> <span data-ttu-id="e31b9-109">Se esse parâmetro for **true**, a janela exibirá texto simples.</span><span class="sxs-lookup"><span data-stu-id="e31b9-109">If this parameter is **TRUE**, the window displays simple text.</span></span> <span data-ttu-id="e31b9-110">Se for **false**, exibirá várias partes.</span><span class="sxs-lookup"><span data-stu-id="e31b9-110">If it is **FALSE**, it displays multiple parts.</span></span>

</dd> <dt>

<span data-ttu-id="e31b9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e31b9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e31b9-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e31b9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e31b9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e31b9-113">Return value</span></span>

<span data-ttu-id="e31b9-114">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="e31b9-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e31b9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e31b9-115">Remarks</span></span>

<span data-ttu-id="e31b9-116">Se a janela de status estiver sendo alterada de não simples para simples, ou vice-versa, a janela será redesenhada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e31b9-116">If the status window is being changed from nonsimple to simple, or vice versa, the window is immediately redrawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31b9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e31b9-117">Requirements</span></span>



| <span data-ttu-id="e31b9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e31b9-118">Requirement</span></span> | <span data-ttu-id="e31b9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e31b9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e31b9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e31b9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e31b9-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e31b9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e31b9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e31b9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e31b9-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e31b9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e31b9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e31b9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e31b9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e31b9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





