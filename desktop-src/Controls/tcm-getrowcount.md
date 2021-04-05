---
title: Mensagem de TCM_GETROWCOUNT (commctrl. h)
description: Recupera o número atual de linhas de guias em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetRowCount TabCtrl.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- Controles de TCM_GETROWCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824711"
---
# <a name="tcm_getrowcount-message"></a><span data-ttu-id="ce21c-105">Mensagem do TCM \_ GETrowcount</span><span class="sxs-lookup"><span data-stu-id="ce21c-105">TCM\_GETROWCOUNT message</span></span>

<span data-ttu-id="ce21c-106">Recupera o número atual de linhas de guias em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="ce21c-106">Retrieves the current number of rows of tabs in a tab control.</span></span> <span data-ttu-id="ce21c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetRowCount TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .</span><span class="sxs-lookup"><span data-stu-id="ce21c-107">You can send this message explicitly or by using the [**TabCtrl\_GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce21c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce21c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce21c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce21c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ce21c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ce21c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ce21c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce21c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ce21c-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ce21c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce21c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce21c-113">Return value</span></span>

<span data-ttu-id="ce21c-114">Retorna o número de linhas de guias.</span><span class="sxs-lookup"><span data-stu-id="ce21c-114">Returns the number of rows of tabs.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce21c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce21c-115">Remarks</span></span>

<span data-ttu-id="ce21c-116">Somente controles de guia que têm o estilo de [**\_ multilinha de TCS**](tab-control-styles.md) podem ter várias linhas de guias.</span><span class="sxs-lookup"><span data-stu-id="ce21c-116">Only tab controls that have the [**TCS\_MULTILINE**](tab-control-styles.md) style can have multiple rows of tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce21c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce21c-117">Requirements</span></span>



| <span data-ttu-id="ce21c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce21c-118">Requirement</span></span> | <span data-ttu-id="ce21c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ce21c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce21c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce21c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ce21c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce21c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce21c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce21c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ce21c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce21c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce21c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce21c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce21c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce21c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





