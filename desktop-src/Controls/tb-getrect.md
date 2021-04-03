---
title: Mensagem de TB_GETRECT (commctrl. h)
description: Recupera o retângulo delimitador para um botão de barra de ferramentas especificado.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- Controles de TB_GETRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824807"
---
# <a name="tb_getrect-message"></a><span data-ttu-id="0ebd2-104">Mensagem de TB \_ GETrect</span><span class="sxs-lookup"><span data-stu-id="0ebd2-104">TB\_GETRECT message</span></span>

<span data-ttu-id="0ebd2-105">Recupera o retângulo delimitador para um botão de barra de ferramentas especificado.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-105">Retrieves the bounding rectangle for a specified toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ebd2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ebd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ebd2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ebd2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebd2-108">Identificador de comando do botão.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="0ebd2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ebd2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebd2-110">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá as informações de retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounding rectangle information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ebd2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ebd2-111">Return value</span></span>

<span data-ttu-id="0ebd2-112">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ebd2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ebd2-113">Remarks</span></span>

<span data-ttu-id="0ebd2-114">Esta mensagem não recupera o retângulo delimitador para botões cujo estado é definido como o [**valor \_ oculto TBSTATE**](toolbar-button-states.md) .</span><span class="sxs-lookup"><span data-stu-id="0ebd2-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebd2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ebd2-115">Requirements</span></span>



| <span data-ttu-id="0ebd2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebd2-116">Requirement</span></span> | <span data-ttu-id="0ebd2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0ebd2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebd2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ebd2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebd2-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ebd2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ebd2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ebd2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebd2-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ebd2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ebd2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ebd2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ebd2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

