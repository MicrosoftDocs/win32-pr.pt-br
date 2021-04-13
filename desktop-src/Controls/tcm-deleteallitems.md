---
title: Mensagem de TCM_DELETEALLITEMS (commctrl. h)
description: Remove todos os itens de um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ DeleteAllItems.
ms.assetid: 733494c4-38f4-44ba-98d2-c33a8d63c3b7
keywords:
- Controles de TCM_DELETEALLITEMS de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b73a91cd6ec3b5472b6e7da2127f8224062cfbbc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499694"
---
# <a name="tcm_deleteallitems-message"></a><span data-ttu-id="faa38-105">\_Mensagem DELETEALLITEMS de TCM</span><span class="sxs-lookup"><span data-stu-id="faa38-105">TCM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="faa38-106">Remove todos os itens de um controle guia.</span><span class="sxs-lookup"><span data-stu-id="faa38-106">Removes all items from a tab control.</span></span> <span data-ttu-id="faa38-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="faa38-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="faa38-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faa38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faa38-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="faa38-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="faa38-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="faa38-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="faa38-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="faa38-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="faa38-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="faa38-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faa38-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="faa38-113">Return value</span></span>

<span data-ttu-id="faa38-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="faa38-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="faa38-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faa38-115">Requirements</span></span>



| <span data-ttu-id="faa38-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="faa38-116">Requirement</span></span> | <span data-ttu-id="faa38-117">Valor</span><span class="sxs-lookup"><span data-stu-id="faa38-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="faa38-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faa38-118">Minimum supported client</span></span><br/> | <span data-ttu-id="faa38-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="faa38-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="faa38-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faa38-120">Minimum supported server</span></span><br/> | <span data-ttu-id="faa38-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="faa38-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="faa38-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="faa38-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="faa38-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="faa38-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





