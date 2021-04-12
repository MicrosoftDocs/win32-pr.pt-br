---
title: Mensagem de HDM_SETORDERARRAY (commctrl. h)
description: Define a ordem da esquerda para a direita dos itens de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetOrderArray do cabeçalho.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- Controles de HDM_SETORDERARRAY de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455232"
---
# <a name="hdm_setorderarray-message"></a><span data-ttu-id="d7e93-105">\_Mensagem HDM SETORDERARRAY</span><span class="sxs-lookup"><span data-stu-id="d7e93-105">HDM\_SETORDERARRAY message</span></span>

<span data-ttu-id="d7e93-106">Define a ordem da esquerda para a direita dos itens de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d7e93-106">Sets the left-to-right order of header items.</span></span> <span data-ttu-id="d7e93-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetOrderArray do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .</span><span class="sxs-lookup"><span data-stu-id="d7e93-107">You can send this message explicitly or use the [**Header\_SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7e93-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7e93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7e93-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7e93-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7e93-110">O tamanho do buffer em *lParam*, em elementos.</span><span class="sxs-lookup"><span data-stu-id="d7e93-110">The size of the buffer at *lParam*, in elements.</span></span> <span data-ttu-id="d7e93-111">Esse valor deve ser igual ao valor retornado por [**HDM \_ GetItemCount**](hdm-getitemcount.md).</span><span class="sxs-lookup"><span data-stu-id="d7e93-111">This value must equal the value returned by [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7e93-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7e93-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7e93-113">Um ponteiro para uma matriz que especifica a ordem na qual os itens devem ser exibidos, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="d7e93-113">A pointer to an array that specifies the order in which items should be displayed, from left to right.</span></span> <span data-ttu-id="d7e93-114">Por exemplo, se o conteúdo da matriz for {2,0,1} , o controle exibirá item 2, item 0 e item 1, da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="d7e93-114">For example, if the contents of the array are {2,0,1}, the control displays item 2, item 0, and item 1, from left to right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7e93-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7e93-115">Return value</span></span>

<span data-ttu-id="d7e93-116">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="d7e93-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7e93-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7e93-117">Requirements</span></span>



| <span data-ttu-id="d7e93-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7e93-118">Requirement</span></span> | <span data-ttu-id="d7e93-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d7e93-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e93-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7e93-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d7e93-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7e93-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7e93-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7e93-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d7e93-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7e93-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7e93-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7e93-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7e93-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7e93-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





