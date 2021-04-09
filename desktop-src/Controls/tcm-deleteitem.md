---
title: Mensagem de TCM_DELETEITEM (commctrl. h)
description: Remove um item de um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ DeleteItem.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- Controles de TCM_DELETEITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919023"
---
# <a name="tcm_deleteitem-message"></a><span data-ttu-id="8beef-105">\_Mensagem DELETEITEM de TCM</span><span class="sxs-lookup"><span data-stu-id="8beef-105">TCM\_DELETEITEM message</span></span>

<span data-ttu-id="8beef-106">Remove um item de um controle guia.</span><span class="sxs-lookup"><span data-stu-id="8beef-106">Removes an item from a tab control.</span></span> <span data-ttu-id="8beef-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="8beef-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8beef-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8beef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8beef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8beef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8beef-110">Índice do item a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="8beef-110">Index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="8beef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8beef-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8beef-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8beef-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8beef-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8beef-113">Return value</span></span>

<span data-ttu-id="8beef-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8beef-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8beef-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8beef-115">Requirements</span></span>



| <span data-ttu-id="8beef-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8beef-116">Requirement</span></span> | <span data-ttu-id="8beef-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8beef-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8beef-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8beef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8beef-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8beef-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8beef-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8beef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8beef-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8beef-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8beef-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8beef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8beef-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8beef-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





