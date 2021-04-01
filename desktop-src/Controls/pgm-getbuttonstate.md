---
title: Mensagem de PGM_GETBUTTONSTATE (commctrl. h)
description: Recupera o estado do botão especificado em um controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Getbuttonstate do pager.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- Controles de PGM_GETBUTTONSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918788"
---
# <a name="pgm_getbuttonstate-message"></a><span data-ttu-id="53f31-105">Mensagem do PGM \_ GETbuttonstate</span><span class="sxs-lookup"><span data-stu-id="53f31-105">PGM\_GETBUTTONSTATE message</span></span>

<span data-ttu-id="53f31-106">Recupera o estado do botão especificado em um controle de pager.</span><span class="sxs-lookup"><span data-stu-id="53f31-106">Retrieves the state of the specified button in a pager control.</span></span> <span data-ttu-id="53f31-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ getbuttonstate do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) .</span><span class="sxs-lookup"><span data-stu-id="53f31-107">You can send this message explicitly or use the [**Pager\_GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="53f31-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53f31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f31-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53f31-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="53f31-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="53f31-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="53f31-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53f31-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53f31-112">Indica para qual botão recuperar o estado.</span><span class="sxs-lookup"><span data-stu-id="53f31-112">Indicates which button to retrieve the state for.</span></span> <span data-ttu-id="53f31-113">Esse valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="53f31-113">This can be one of the following values:</span></span>



| <span data-ttu-id="53f31-114">Valor</span><span class="sxs-lookup"><span data-stu-id="53f31-114">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="53f31-115">Significado</span><span class="sxs-lookup"><span data-stu-id="53f31-115">Meaning</span></span>                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <span data-ttu-id="53f31-116"><dt>**PGB \_ TOPORLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="53f31-116"><dt>**PGB\_TOPORLEFT**</dt></span></span> </dl>             | <span data-ttu-id="53f31-117">Indica o botão superior em um controle de pager [**\_ Vert PGS**](pager-control-styles.md) ou o botão esquerdo em um controle [**PGS \_ na horizontal**](pager-control-styles.md) pager.</span><span class="sxs-lookup"><span data-stu-id="53f31-117">Indicates the top button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the left button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <span data-ttu-id="53f31-118"><dt>**PGB \_ BOTTOMORRIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="53f31-118"><dt>**PGB\_BOTTOMORRIGHT**</dt></span></span> </dl> | <span data-ttu-id="53f31-119">Indica o botão inferior em um controle de pager [**\_ Vert PGS**](pager-control-styles.md) ou o botão direito em um controle [**PGS \_ na horizontal**](pager-control-styles.md) pager.</span><span class="sxs-lookup"><span data-stu-id="53f31-119">Indicates the bottom button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the right button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f31-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53f31-120">Return value</span></span>

<span data-ttu-id="53f31-121">Retorna o estado do botão especificado em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="53f31-121">Returns the state of the button specified in *lParam*.</span></span> <span data-ttu-id="53f31-122">Esse será um ou mais dos seguintes valores (se mais de um valor for retornado, eles serão combinados usando um OR bit a bit):</span><span class="sxs-lookup"><span data-stu-id="53f31-122">This will be one or more of the following values (if more then one value is returned they will be combined using a bitwise OR):</span></span>



| <span data-ttu-id="53f31-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="53f31-123">Return code</span></span>                                                                                   | <span data-ttu-id="53f31-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="53f31-124">Description</span></span>                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="53f31-125"><dt>**PGF \_ invisível**</dt></span><span class="sxs-lookup"><span data-stu-id="53f31-125"><dt>**PGF\_INVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="53f31-126">O botão não está visível.</span><span class="sxs-lookup"><span data-stu-id="53f31-126">The button is not visible.</span></span> <br/>      |
| <dl> <span data-ttu-id="53f31-127"><dt>**PGF \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="53f31-127"><dt>**PGF\_NORMAL**</dt></span></span> </dl>    | <span data-ttu-id="53f31-128">O botão está em estado normal.</span><span class="sxs-lookup"><span data-stu-id="53f31-128">The button is in normal state.</span></span> <br/>  |
| <dl> <span data-ttu-id="53f31-129"><dt>**PGF \_ cinza**</dt></span><span class="sxs-lookup"><span data-stu-id="53f31-129"><dt>**PGF\_GRAYED**</dt></span></span> </dl>    | <span data-ttu-id="53f31-130">O botão está em estado acinzentado.</span><span class="sxs-lookup"><span data-stu-id="53f31-130">The button is in grayed state.</span></span> <br/>  |
| <dl> <span data-ttu-id="53f31-131"><dt>**PGF \_ pressionado**</dt></span><span class="sxs-lookup"><span data-stu-id="53f31-131"><dt>**PGF\_DEPRESSED**</dt></span></span> </dl> | <span data-ttu-id="53f31-132">O botão está no estado pressionado.</span><span class="sxs-lookup"><span data-stu-id="53f31-132">The button is in pressed state.</span></span> <br/> |
| <dl> <span data-ttu-id="53f31-133"><dt>**PGF \_ quente**</dt></span><span class="sxs-lookup"><span data-stu-id="53f31-133"><dt>**PGF\_HOT**</dt></span></span> </dl>       | <span data-ttu-id="53f31-134">O botão está em estado ativo.</span><span class="sxs-lookup"><span data-stu-id="53f31-134">The button is in hot state.</span></span> <br/>     |



 

## <a name="requirements"></a><span data-ttu-id="53f31-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53f31-135">Requirements</span></span>



| <span data-ttu-id="53f31-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="53f31-136">Requirement</span></span> | <span data-ttu-id="53f31-137">Valor</span><span class="sxs-lookup"><span data-stu-id="53f31-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53f31-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53f31-138">Minimum supported client</span></span><br/> | <span data-ttu-id="53f31-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53f31-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53f31-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53f31-140">Minimum supported server</span></span><br/> | <span data-ttu-id="53f31-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53f31-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53f31-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53f31-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="53f31-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f31-143"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





