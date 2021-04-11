---
title: Mensagem de HDM_DELETEITEM (commctrl. h)
description: Exclui um item de um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro DeleteItem do cabeçalho.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- Controles de HDM_DELETEITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009525"
---
# <a name="hdm_deleteitem-message"></a><span data-ttu-id="7a51b-105">\_Mensagem HDM DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="7a51b-105">HDM\_DELETEITEM message</span></span>

<span data-ttu-id="7a51b-106">Exclui um item de um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="7a51b-106">Deletes an item from a header control.</span></span> <span data-ttu-id="7a51b-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ DeleteItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="7a51b-107">You can send this message explicitly or use the [**Header\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a51b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a51b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a51b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a51b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a51b-110">Um índice do item a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7a51b-110">An index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="7a51b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a51b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7a51b-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7a51b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a51b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a51b-113">Return value</span></span>

<span data-ttu-id="7a51b-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7a51b-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a51b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a51b-115">Requirements</span></span>



| <span data-ttu-id="7a51b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a51b-116">Requirement</span></span> | <span data-ttu-id="7a51b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7a51b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a51b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a51b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a51b-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a51b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a51b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a51b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a51b-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a51b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a51b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a51b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a51b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a51b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





