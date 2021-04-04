---
title: Mensagem de TB_GETITEMRECT (commctrl. h)
description: Recupera o retângulo delimitador de um botão em uma barra de ferramentas.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- Controles de TB_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824617"
---
# <a name="tb_getitemrect-message"></a><span data-ttu-id="1b5ca-104">TB de \_ mensagem GETITEMRECT</span><span class="sxs-lookup"><span data-stu-id="1b5ca-104">TB\_GETITEMRECT message</span></span>

<span data-ttu-id="1b5ca-105">Recupera o retângulo delimitador de um botão em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="1b5ca-105">Retrieves the bounding rectangle of a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b5ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b5ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b5ca-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b5ca-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b5ca-108">Índice de base zero do botão para o qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="1b5ca-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="1b5ca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b5ca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b5ca-110">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe as coordenadas de cliente do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="1b5ca-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the client coordinates of the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b5ca-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b5ca-111">Return value</span></span>

<span data-ttu-id="1b5ca-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="1b5ca-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b5ca-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b5ca-113">Remarks</span></span>

<span data-ttu-id="1b5ca-114">Esta mensagem não recupera o retângulo delimitador para botões cujo estado é definido como o [**valor \_ oculto TBSTATE**](toolbar-button-states.md) .</span><span class="sxs-lookup"><span data-stu-id="1b5ca-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b5ca-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b5ca-115">Requirements</span></span>



| <span data-ttu-id="1b5ca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b5ca-116">Requirement</span></span> | <span data-ttu-id="1b5ca-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1b5ca-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b5ca-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b5ca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b5ca-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b5ca-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b5ca-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b5ca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b5ca-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b5ca-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b5ca-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b5ca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b5ca-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b5ca-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

