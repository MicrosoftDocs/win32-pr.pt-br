---
title: Mensagem de SB_GETPARTS (commctrl. h)
description: Recupera uma contagem das partes em uma janela de status. A mensagem também recupera a coordenada da borda direita do número especificado de partes.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- Controles de SB_GETPARTS de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499597"
---
# <a name="sb_getparts-message"></a><span data-ttu-id="90905-105">Mensagem da SB \_ GETparts</span><span class="sxs-lookup"><span data-stu-id="90905-105">SB\_GETPARTS message</span></span>

<span data-ttu-id="90905-106">Recupera uma contagem das partes em uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="90905-106">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="90905-107">A mensagem também recupera a coordenada da borda direita do número especificado de partes.</span><span class="sxs-lookup"><span data-stu-id="90905-107">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span>

## <a name="parameters"></a><span data-ttu-id="90905-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90905-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90905-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90905-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90905-110">Número de partes para as quais recuperar as coordenadas.</span><span class="sxs-lookup"><span data-stu-id="90905-110">Number of parts for which to retrieve coordinates.</span></span> <span data-ttu-id="90905-111">Se esse parâmetro for maior que o número de partes na janela, a mensagem recuperará coordenadas somente para partes existentes.</span><span class="sxs-lookup"><span data-stu-id="90905-111">If this parameter is greater than the number of parts in the window, the message retrieves coordinates for existing parts only.</span></span>

</dd> <dt>

<span data-ttu-id="90905-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90905-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90905-113">Ponteiro para uma matriz de inteiros que tem o mesmo número de elementos que as partes especificadas por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="90905-113">Pointer to an integer array that has the same number of elements as parts specified by *wParam*.</span></span> <span data-ttu-id="90905-114">Cada elemento na matriz recebe a coordenada do cliente da borda direita da parte correspondente.</span><span class="sxs-lookup"><span data-stu-id="90905-114">Each element in the array receives the client coordinate of the right edge of the corresponding part.</span></span> <span data-ttu-id="90905-115">Se um elemento for definido como-1, a posição da borda direita dessa parte se estenderá para a borda direita da janela.</span><span class="sxs-lookup"><span data-stu-id="90905-115">If an element is set to -1, the position of the right edge for that part extends to the right edge of the window.</span></span> <span data-ttu-id="90905-116">Para recuperar o número atual de partes, defina esse parâmetro como zero.</span><span class="sxs-lookup"><span data-stu-id="90905-116">To retrieve the current number of parts, set this parameter to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90905-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90905-117">Return value</span></span>

<span data-ttu-id="90905-118">Retorna o número de partes na janela.</span><span class="sxs-lookup"><span data-stu-id="90905-118">Returns the number of parts in the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="90905-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="90905-119">Remarks</span></span>

<span data-ttu-id="90905-120">Essa mensagem sempre retorna o número de partes na barra de status.</span><span class="sxs-lookup"><span data-stu-id="90905-120">This message always returns the number of parts in the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="90905-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90905-121">Requirements</span></span>



| <span data-ttu-id="90905-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="90905-122">Requirement</span></span> | <span data-ttu-id="90905-123">Valor</span><span class="sxs-lookup"><span data-stu-id="90905-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90905-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90905-124">Minimum supported client</span></span><br/> | <span data-ttu-id="90905-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90905-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90905-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90905-126">Minimum supported server</span></span><br/> | <span data-ttu-id="90905-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90905-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90905-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90905-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="90905-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90905-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





