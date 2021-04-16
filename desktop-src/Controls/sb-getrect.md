---
title: Mensagem de SB_GETRECT (commctrl. h)
description: Recupera o retângulo delimitador de uma parte em uma janela de status.
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- Controles de SB_GETRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48808b7bdf9c97fa6b9da53112e505e8cb8e66e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455608"
---
# <a name="sb_getrect-message"></a><span data-ttu-id="9ff4c-104">\_Mensagem de GETRECT SB</span><span class="sxs-lookup"><span data-stu-id="9ff4c-104">SB\_GETRECT message</span></span>

<span data-ttu-id="9ff4c-105">Recupera o retângulo delimitador de uma parte em uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="9ff4c-105">Retrieves the bounding rectangle of a part in a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ff4c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ff4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff4c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ff4c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ff4c-108">Índice de base zero da parte cujo retângulo delimitador deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="9ff4c-108">Zero-based index of the part whose bounding rectangle is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="9ff4c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ff4c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ff4c-110">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="9ff4c-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff4c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ff4c-111">Return value</span></span>

<span data-ttu-id="9ff4c-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9ff4c-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff4c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ff4c-113">Requirements</span></span>



| <span data-ttu-id="9ff4c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ff4c-114">Requirement</span></span> | <span data-ttu-id="9ff4c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9ff4c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff4c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ff4c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff4c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ff4c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ff4c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ff4c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff4c-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ff4c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ff4c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ff4c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff4c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff4c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

