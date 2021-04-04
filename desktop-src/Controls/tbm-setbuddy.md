---
title: Mensagem de TBM_SETBUDDY (commctrl. h)
description: Atribui uma janela como a janela Buddy para um controle TrackBar. As janelas TrackBar Buddy são exibidas automaticamente em um local em relação à orientação do controle (horizontal ou vertical).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- Controles de TBM_SETBUDDY de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009068"
---
# <a name="tbm_setbuddy-message"></a><span data-ttu-id="a3574-105">Mensagem do TBM \_ SETbuddy</span><span class="sxs-lookup"><span data-stu-id="a3574-105">TBM\_SETBUDDY message</span></span>

<span data-ttu-id="a3574-106">Atribui uma janela como a janela Buddy para um controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a3574-106">Assigns a window as the buddy window for a trackbar control.</span></span> <span data-ttu-id="a3574-107">As janelas TrackBar Buddy são exibidas automaticamente em um local em relação à orientação do controle (horizontal ou vertical).</span><span class="sxs-lookup"><span data-stu-id="a3574-107">Trackbar buddy windows are automatically displayed in a location relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="a3574-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3574-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3574-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3574-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3574-110">Valor que especifica o local no qual exibir a janela do Buddy.</span><span class="sxs-lookup"><span data-stu-id="a3574-110">Value specifying the location at which to display the buddy window.</span></span> <span data-ttu-id="a3574-111">Este valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="a3574-111">This value can be one of the following:</span></span>



| <span data-ttu-id="a3574-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a3574-112">Value</span></span>                                                                                                                                | <span data-ttu-id="a3574-113">Significado</span><span class="sxs-lookup"><span data-stu-id="a3574-113">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="a3574-114"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="a3574-114"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="a3574-115">O colega será exibido à esquerda do TrackBar se o controle TrackBar usar o estilo [**TBS \_ na horizontal**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3574-115">The buddy will appear to the left of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="a3574-116">Se o TrackBar usar o [**estilo \_ vertical do TBS**](trackbar-control-styles.md) , o colega aparecerá acima do controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a3574-116">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears above the trackbar control.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="a3574-117"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="a3574-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="a3574-118">O colega será exibido à direita de TrackBar se o controle TrackBar usar o estilo [**TBS \_ na horizontal**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3574-118">The buddy will appear to the right of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="a3574-119">Se o TrackBar usar o [**estilo \_ vertical do TBS**](trackbar-control-styles.md) , o colega aparecerá abaixo do controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a3574-119">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears below the trackbar control.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a3574-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3574-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3574-121">Manipule para a janela que será definida como o colega do controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a3574-121">Handle to the window that will be set as the trackbar control's buddy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3574-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3574-122">Return value</span></span>

<span data-ttu-id="a3574-123">Retorna o identificador para a janela que foi atribuída anteriormente ao controle nesse local.</span><span class="sxs-lookup"><span data-stu-id="a3574-123">Returns the handle to the window that was previously assigned to the control at that location.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3574-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3574-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a3574-125">Os controles TrackBar dão suporte a até duas janelas de amigo.</span><span class="sxs-lookup"><span data-stu-id="a3574-125">Trackbar controls support up to two buddy windows.</span></span> <span data-ttu-id="a3574-126">Isso pode ser útil quando você precisa exibir texto ou imagens em cada extremidade do controle.</span><span class="sxs-lookup"><span data-stu-id="a3574-126">This can be useful when you must display text or images at each end of the control.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a3574-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3574-127">Requirements</span></span>



| <span data-ttu-id="a3574-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3574-128">Requirement</span></span> | <span data-ttu-id="a3574-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a3574-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3574-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3574-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a3574-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3574-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3574-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3574-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a3574-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a3574-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3574-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3574-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3574-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3574-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





