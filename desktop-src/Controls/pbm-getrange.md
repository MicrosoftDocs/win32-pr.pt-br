---
title: Mensagem de PBM_GETRANGE (commctrl. h)
description: Recupera informações sobre os limites altos e baixos atuais de um determinado controle de barra de progresso.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- Controles de PBM_GETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918795"
---
# <a name="pbm_getrange-message"></a><span data-ttu-id="398b4-104">\_Mensagem GETrange do PBM</span><span class="sxs-lookup"><span data-stu-id="398b4-104">PBM\_GETRANGE message</span></span>

<span data-ttu-id="398b4-105">Recupera informações sobre os limites altos e baixos atuais de um determinado controle de barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="398b4-105">Retrieves information about the current high and low limits of a given progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="398b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="398b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="398b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="398b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="398b4-108">Valor do sinalizador que especifica qual valor de limite deve ser usado como o valor de retorno da mensagem.</span><span class="sxs-lookup"><span data-stu-id="398b4-108">Flag value specifying which limit value is to be used as the message's return value.</span></span> <span data-ttu-id="398b4-109">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="398b4-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="398b4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="398b4-110">Value</span></span>                                                                                                                                    | <span data-ttu-id="398b4-111">Significado</span><span class="sxs-lookup"><span data-stu-id="398b4-111">Meaning</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="398b4-112"><dt>VERDADEIRO \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="398b4-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="398b4-113">Retornar o limite baixo.</span><span class="sxs-lookup"><span data-stu-id="398b4-113">Return the low limit.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="398b4-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="398b4-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="398b4-115">Retornar o limite alto.</span><span class="sxs-lookup"><span data-stu-id="398b4-115">Return the high limit.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="398b4-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="398b4-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="398b4-117">Ponteiro para uma estrutura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que deve ser preenchida com os limites alto e baixo do controle de barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="398b4-117">Pointer to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with the high and low limits of the progress bar control.</span></span> <span data-ttu-id="398b4-118">Se esse parâmetro for definido como **NULL**, o controle retornará apenas o limite especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="398b4-118">If this parameter is set to **NULL**, the control will return only the limit specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="398b4-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="398b4-119">Return value</span></span>

<span data-ttu-id="398b4-120">Retorna um INT que representa o valor de limite especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="398b4-120">Returns an INT that represents the limit value specified by *wParam*.</span></span> <span data-ttu-id="398b4-121">Se *lParam* não for **NULL**, *lParam* deverá apontar para uma estrutura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que será preenchida com ambos os valores de limite.</span><span class="sxs-lookup"><span data-stu-id="398b4-121">If *lParam* is not **NULL**, *lParam* must point to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with both limit values.</span></span>

## <a name="requirements"></a><span data-ttu-id="398b4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="398b4-122">Requirements</span></span>



| <span data-ttu-id="398b4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="398b4-123">Requirement</span></span> | <span data-ttu-id="398b4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="398b4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="398b4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="398b4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="398b4-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="398b4-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="398b4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="398b4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="398b4-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="398b4-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="398b4-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="398b4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="398b4-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="398b4-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





