---
title: Mensagem de SB_GETBORDERS (commctrl. h)
description: Recupera as larguras atuais das bordas horizontais e verticais de uma janela de status.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- Controles de SB_GETBORDERS de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086023"
---
# <a name="sb_getborders-message"></a><span data-ttu-id="8d5aa-104">Mensagem da SB \_ GETborders</span><span class="sxs-lookup"><span data-stu-id="8d5aa-104">SB\_GETBORDERS message</span></span>

<span data-ttu-id="8d5aa-105">Recupera as larguras atuais das bordas horizontais e verticais de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="8d5aa-105">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d5aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d5aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d5aa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d5aa-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8d5aa-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8d5aa-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8d5aa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d5aa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d5aa-110">Ponteiro para uma matriz de inteiros que tem três elementos.</span><span class="sxs-lookup"><span data-stu-id="8d5aa-110">Pointer to an integer array that has three elements.</span></span> <span data-ttu-id="8d5aa-111">O primeiro elemento recebe a largura da borda horizontal, a segunda recebe a largura da borda vertical e a terceira recebe a largura da borda entre retângulos.</span><span class="sxs-lookup"><span data-stu-id="8d5aa-111">The first element receives the width of the horizontal border, the second receives the width of the vertical border, and the third receives the width of the border between rectangles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d5aa-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d5aa-112">Return value</span></span>

<span data-ttu-id="8d5aa-113">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8d5aa-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d5aa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d5aa-114">Remarks</span></span>

<span data-ttu-id="8d5aa-115">As bordas determinam o espaçamento entre a borda externa da janela e os retângulos dentro da janela que contêm texto.</span><span class="sxs-lookup"><span data-stu-id="8d5aa-115">The borders determine the spacing between the outside edge of the window and the rectangles within the window that contain text.</span></span> <span data-ttu-id="8d5aa-116">As bordas também determinam o espaçamento entre retângulos.</span><span class="sxs-lookup"><span data-stu-id="8d5aa-116">The borders also determine the spacing between rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d5aa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d5aa-117">Requirements</span></span>



| <span data-ttu-id="8d5aa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d5aa-118">Requirement</span></span> | <span data-ttu-id="8d5aa-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8d5aa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5aa-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d5aa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d5aa-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d5aa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d5aa-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d5aa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d5aa-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d5aa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d5aa-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d5aa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d5aa-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d5aa-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





