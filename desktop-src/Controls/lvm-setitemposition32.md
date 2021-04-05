---
title: Mensagem de LVM_SETITEMPOSITION32 (commctrl. h)
description: Move um item para uma posição especificada em um controle de exibição de lista (deve estar no ícone ou exibição de ícone pequeno).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- Controles de LVM_SETITEMPOSITION32 de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009426"
---
# <a name="lvm_setitemposition32-message"></a><span data-ttu-id="764e2-104">\_Mensagem SETITEMPOSITION32 LVM</span><span class="sxs-lookup"><span data-stu-id="764e2-104">LVM\_SETITEMPOSITION32 message</span></span>

<span data-ttu-id="764e2-105">Move um item para uma posição especificada em um controle de exibição de lista (deve estar no ícone ou exibição de ícone pequeno).</span><span class="sxs-lookup"><span data-stu-id="764e2-105">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="764e2-106">Essa mensagem difere da mensagem [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) , pois usa coordenadas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="764e2-106">This message differs from the [**LVM\_SETITEMPOSITION**](lvm-setitemposition.md) message in that it uses 32-bit coordinates.</span></span> <span data-ttu-id="764e2-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItemPosition32 do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .</span><span class="sxs-lookup"><span data-stu-id="764e2-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="764e2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="764e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="764e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="764e2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="764e2-110">Índice do item de exibição de lista para o qual definir a posição.</span><span class="sxs-lookup"><span data-stu-id="764e2-110">Index of the list-view item for which to set the position.</span></span>

</dd> <dt>

<span data-ttu-id="764e2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="764e2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="764e2-112">Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que contém a nova posição do item, em coordenadas de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="764e2-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the new position of the item, in list-view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="764e2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="764e2-113">Return value</span></span>

<span data-ttu-id="764e2-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="764e2-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="764e2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="764e2-115">Requirements</span></span>



| <span data-ttu-id="764e2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="764e2-116">Requirement</span></span> | <span data-ttu-id="764e2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="764e2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="764e2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="764e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="764e2-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="764e2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="764e2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="764e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="764e2-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="764e2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="764e2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="764e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="764e2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="764e2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

