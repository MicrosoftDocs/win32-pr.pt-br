---
title: Mensagem de TCM_GETITEMCOUNT (commctrl. h)
description: Recupera o número de guias no controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ GetItemCount.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- Controles de TCM_GETITEMCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086243"
---
# <a name="tcm_getitemcount-message"></a><span data-ttu-id="51558-105">Mensagem do TCM \_ GETitemcount</span><span class="sxs-lookup"><span data-stu-id="51558-105">TCM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="51558-106">Recupera o número de guias no controle guia.</span><span class="sxs-lookup"><span data-stu-id="51558-106">Retrieves the number of tabs in the tab control.</span></span> <span data-ttu-id="51558-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="51558-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="51558-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51558-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51558-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51558-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="51558-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="51558-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="51558-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51558-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="51558-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="51558-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51558-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51558-113">Return value</span></span>

<span data-ttu-id="51558-114">Retorna o número de itens, se for bem-sucedido, ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="51558-114">Returns the number of items if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="51558-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51558-115">Requirements</span></span>



| <span data-ttu-id="51558-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="51558-116">Requirement</span></span> | <span data-ttu-id="51558-117">Valor</span><span class="sxs-lookup"><span data-stu-id="51558-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51558-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51558-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51558-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51558-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51558-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51558-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51558-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51558-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51558-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51558-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="51558-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="51558-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





