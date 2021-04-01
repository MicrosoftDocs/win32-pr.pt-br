---
title: Mensagem de LVM_SETHOTCURSOR (commctrl. h)
description: Define o valor de HCURSOR que o controle de exibição de lista usa quando o ponteiro está sobre um item enquanto o controle ativo está habilitado.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- Controles de LVM_SETHOTCURSOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644261"
---
# <a name="lvm_sethotcursor-message"></a><span data-ttu-id="d11bc-104">\_Mensagem SETHOTCURSOR LVM</span><span class="sxs-lookup"><span data-stu-id="d11bc-104">LVM\_SETHOTCURSOR message</span></span>

<span data-ttu-id="d11bc-105">Define o valor de HCURSOR que o controle de exibição de lista usa quando o ponteiro está sobre um item enquanto o controle ativo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d11bc-105">Sets the HCURSOR value that the list-view control uses when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="d11bc-106">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetHotCursor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="d11bc-106">You can send this message explicitly or use the [**ListView\_SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) macro.</span></span> <span data-ttu-id="d11bc-107">Para verificar se o rastreamento dinâmico está habilitado, chame [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="d11bc-107">To check whether hot tracking is enabled, call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span>

## <a name="parameters"></a><span data-ttu-id="d11bc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d11bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d11bc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d11bc-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d11bc-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d11bc-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d11bc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d11bc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d11bc-112">Identificador para o cursor a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d11bc-112">Handle to the cursor to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d11bc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d11bc-113">Return value</span></span>

<span data-ttu-id="d11bc-114">Retorna um valor HCURSOR que é o cursor quente anterior.</span><span class="sxs-lookup"><span data-stu-id="d11bc-114">Returns an HCURSOR value that is the previous hot cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="d11bc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d11bc-115">Remarks</span></span>

<span data-ttu-id="d11bc-116">Um controle de exibição de lista usa rastreamento dinâmico e seleção de foco quando o estilo [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) é definido.</span><span class="sxs-lookup"><span data-stu-id="d11bc-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d11bc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d11bc-117">Requirements</span></span>



| <span data-ttu-id="d11bc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d11bc-118">Requirement</span></span> | <span data-ttu-id="d11bc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d11bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d11bc-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d11bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d11bc-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d11bc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d11bc-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d11bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d11bc-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d11bc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d11bc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d11bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d11bc-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d11bc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

