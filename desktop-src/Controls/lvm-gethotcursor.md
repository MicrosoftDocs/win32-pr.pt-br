---
title: Mensagem de LVM_GETHOTCURSOR (commctrl. h)
description: Recupera o valor HCURSOR usado quando o ponteiro está sobre um item enquanto o controle ativo está habilitado. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetHotCursor do ListView.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- Controles de LVM_GETHOTCURSOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645026"
---
# <a name="lvm_gethotcursor-message"></a><span data-ttu-id="9985c-105">\_Mensagem GETHOTCURSOR LVM</span><span class="sxs-lookup"><span data-stu-id="9985c-105">LVM\_GETHOTCURSOR message</span></span>

<span data-ttu-id="9985c-106">Recupera o valor HCURSOR usado quando o ponteiro está sobre um item enquanto o controle ativo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9985c-106">Retrieves the HCURSOR value used when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="9985c-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetHotCursor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="9985c-107">You can send this message explicitly or use the [**ListView\_GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9985c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9985c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9985c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9985c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9985c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9985c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9985c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9985c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9985c-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9985c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9985c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9985c-113">Return value</span></span>

<span data-ttu-id="9985c-114">Retorna um valor HCURSOR que é o identificador para o cursor que o controle List-View usa quando o controle de acesso está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9985c-114">Returns an HCURSOR value that is the handle to the cursor that the list-view control uses when hot tracking is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="9985c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9985c-115">Remarks</span></span>

<span data-ttu-id="9985c-116">Um controle de exibição de lista usa rastreamento dinâmico e seleção de foco quando o estilo [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) é definido.</span><span class="sxs-lookup"><span data-stu-id="9985c-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="9985c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9985c-117">Requirements</span></span>



| <span data-ttu-id="9985c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9985c-118">Requirement</span></span> | <span data-ttu-id="9985c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9985c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9985c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9985c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9985c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9985c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9985c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9985c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9985c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9985c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9985c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9985c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9985c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9985c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





