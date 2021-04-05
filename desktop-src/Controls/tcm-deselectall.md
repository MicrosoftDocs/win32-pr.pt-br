---
title: Mensagem de TCM_DESELECTALL (commctrl. h)
description: Redefine os itens em um controle guia, limpando os que foram definidos para o \_ estado TCIS ButtonPressed. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ DeselectAll.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- Controles de TCM_DESELECTALL de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086245"
---
# <a name="tcm_deselectall-message"></a><span data-ttu-id="664b4-105">\_Mensagem DESELECTALL de TCM</span><span class="sxs-lookup"><span data-stu-id="664b4-105">TCM\_DESELECTALL message</span></span>

<span data-ttu-id="664b4-106">Redefine os itens em um controle guia, limpando os que foram definidos para o estado [**TCIS \_ ButtonPressed**](tab-control-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="664b4-106">Resets items in a tab control, clearing any that were set to the [**TCIS\_BUTTONPRESSED**](tab-control-item-states.md) state.</span></span> <span data-ttu-id="664b4-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) .</span><span class="sxs-lookup"><span data-stu-id="664b4-107">You can send this message explicitly or by using the [**TabCtrl\_DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="664b4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="664b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="664b4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="664b4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="664b4-110">Sinalizador que especifica o escopo da desmarcação do item.</span><span class="sxs-lookup"><span data-stu-id="664b4-110">Flag that specifies the scope of the item deselection.</span></span> <span data-ttu-id="664b4-111">Se esse parâmetro for definido como **false**, todos os itens da guia serão redefinidos.</span><span class="sxs-lookup"><span data-stu-id="664b4-111">If this parameter is set to **FALSE**, all tab items will be reset.</span></span> <span data-ttu-id="664b4-112">Se estiver definido como **true**, todos os itens da guia, exceto o selecionado no momento, serão redefinidos.</span><span class="sxs-lookup"><span data-stu-id="664b4-112">If it is set to **TRUE**, then all tab items except for the one currently selected will be reset.</span></span>

</dd> <dt>

<span data-ttu-id="664b4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="664b4-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="664b4-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="664b4-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="664b4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="664b4-115">Return value</span></span>

<span data-ttu-id="664b4-116">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="664b4-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="664b4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="664b4-117">Remarks</span></span>

<span data-ttu-id="664b4-118">Essa mensagem só será significativa se o sinalizador de estilo de [**\_ botões de TCS**](tab-control-styles.md) tiver sido definido.</span><span class="sxs-lookup"><span data-stu-id="664b4-118">This message is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span>

## <a name="requirements"></a><span data-ttu-id="664b4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="664b4-119">Requirements</span></span>



| <span data-ttu-id="664b4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="664b4-120">Requirement</span></span> | <span data-ttu-id="664b4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="664b4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="664b4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="664b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="664b4-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="664b4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="664b4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="664b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="664b4-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="664b4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="664b4-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="664b4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="664b4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="664b4-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





