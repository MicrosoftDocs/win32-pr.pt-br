---
title: Mensagem de SB_SETPARTS (commctrl. h)
description: Define o número de partes em uma janela de status e a coordenada da borda direita de cada parte.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- Controles de SB_SETPARTS de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499594"
---
# <a name="sb_setparts-message"></a><span data-ttu-id="1fe5e-104">\_Mensagem de CONpartes da SB</span><span class="sxs-lookup"><span data-stu-id="1fe5e-104">SB\_SETPARTS message</span></span>

<span data-ttu-id="1fe5e-105">Define o número de partes em uma janela de status e a coordenada da borda direita de cada parte.</span><span class="sxs-lookup"><span data-stu-id="1fe5e-105">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span>

## <a name="parameters"></a><span data-ttu-id="1fe5e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fe5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fe5e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1fe5e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fe5e-108">Número de partes a serem definidas (não pode ser maior que 256).</span><span class="sxs-lookup"><span data-stu-id="1fe5e-108">Number of parts to set (cannot be greater than 256).</span></span>

</dd> <dt>

<span data-ttu-id="1fe5e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fe5e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fe5e-110">Ponteiro para uma matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="1fe5e-110">Pointer to an integer array.</span></span> <span data-ttu-id="1fe5e-111">O número de elementos é especificado em *wParam*.</span><span class="sxs-lookup"><span data-stu-id="1fe5e-111">The number of elements is specified in *wParam*.</span></span> <span data-ttu-id="1fe5e-112">Cada elemento Especifica a posição, nas coordenadas do cliente, da borda direita da parte correspondente.</span><span class="sxs-lookup"><span data-stu-id="1fe5e-112">Each element specifies the position, in client coordinates, of the right edge of the corresponding part.</span></span> <span data-ttu-id="1fe5e-113">Se um elemento for-1, a borda direita da parte correspondente se estenderá à borda da janela.</span><span class="sxs-lookup"><span data-stu-id="1fe5e-113">If an element is -1, the right edge of the corresponding part extends to the border of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fe5e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fe5e-114">Return value</span></span>

<span data-ttu-id="1fe5e-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="1fe5e-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe5e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fe5e-116">Requirements</span></span>



| <span data-ttu-id="1fe5e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fe5e-117">Requirement</span></span> | <span data-ttu-id="1fe5e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1fe5e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe5e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fe5e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe5e-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1fe5e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1fe5e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fe5e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe5e-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fe5e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1fe5e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fe5e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fe5e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fe5e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





