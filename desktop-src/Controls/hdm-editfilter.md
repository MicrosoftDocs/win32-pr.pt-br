---
title: Mensagem de HDM_EDITFILTER (commctrl. h)
description: Move o foco de entrada para a caixa de edição quando um botão de filtro tem o foco.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- Controles de HDM_EDITFILTER de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644845"
---
# <a name="hdm_editfilter-message"></a><span data-ttu-id="f14fe-104">\_Mensagem HDM EDITFILTER</span><span class="sxs-lookup"><span data-stu-id="f14fe-104">HDM\_EDITFILTER message</span></span>

<span data-ttu-id="f14fe-105">Move o foco de entrada para a caixa de edição quando um botão de filtro tem o foco.</span><span class="sxs-lookup"><span data-stu-id="f14fe-105">Moves the input focus to the edit box when a filter button has the focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="f14fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f14fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f14fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f14fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f14fe-108">Um valor que especifica a coluna a ser editada.</span><span class="sxs-lookup"><span data-stu-id="f14fe-108">A value specifying the column to edit.</span></span>

</dd> <dt>

<span data-ttu-id="f14fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f14fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f14fe-110">Um sinalizador que especifica como tratar as alterações de edição do usuário.</span><span class="sxs-lookup"><span data-stu-id="f14fe-110">A flag that specifies how to handle the user's editing changes.</span></span> <span data-ttu-id="f14fe-111">Use esse sinalizador para especificar o que fazer se o usuário estiver no processo de edição do filtro quando a mensagem for enviada.</span><span class="sxs-lookup"><span data-stu-id="f14fe-111">Use this flag to specify what to do if the user is in the process of editing the filter when the message is sent.</span></span>



| <span data-ttu-id="f14fe-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f14fe-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="f14fe-113">Significado</span><span class="sxs-lookup"><span data-stu-id="f14fe-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="f14fe-114"><dt></dt><dt> **Verdadeiro**</dt></span><span class="sxs-lookup"><span data-stu-id="f14fe-114"><dt></dt> <dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="f14fe-115">Descarte as alterações feitas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f14fe-115">Discard the changes made by the user.</span></span> <br/> |
| <dl> <span data-ttu-id="f14fe-116"><dt></dt><dt> **Falso**</dt></span><span class="sxs-lookup"><span data-stu-id="f14fe-116"><dt></dt> <dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="f14fe-117">Aceite as alterações feitas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f14fe-117">Accept the changes made by the user.</span></span> <br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f14fe-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f14fe-118">Return value</span></span>

<span data-ttu-id="f14fe-119">Retorna um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="f14fe-119">Returns an integer.</span></span> <span data-ttu-id="f14fe-120">O **LRESULT** é convertido em um inteiro que indica **true**(1) ou **false**(0).</span><span class="sxs-lookup"><span data-stu-id="f14fe-120">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="requirements"></a><span data-ttu-id="f14fe-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f14fe-121">Requirements</span></span>



| <span data-ttu-id="f14fe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f14fe-122">Requirement</span></span> | <span data-ttu-id="f14fe-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f14fe-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f14fe-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f14fe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f14fe-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f14fe-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f14fe-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f14fe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f14fe-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f14fe-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f14fe-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f14fe-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f14fe-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f14fe-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f14fe-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f14fe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14fe-131">**HDM \_ CLEARFILTER**</span><span class="sxs-lookup"><span data-stu-id="f14fe-131">**HDM\_CLEARFILTER**</span></span>](hdm-clearfilter.md)
</dt> </dl>

 

 





