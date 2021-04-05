---
title: Mensagem de TBM_GETBUDDY (commctrl. h)
description: Recupera o identificador para uma janela de amigo do controle TrackBar em um determinado local. O local especificado é relativo à orientação do controle (horizontal ou vertical).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- Controles de TBM_GETBUDDY de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919226"
---
# <a name="tbm_getbuddy-message"></a><span data-ttu-id="f1621-105">Mensagem do TBM \_ GETbuddy</span><span class="sxs-lookup"><span data-stu-id="f1621-105">TBM\_GETBUDDY message</span></span>

<span data-ttu-id="f1621-106">Recupera o identificador para uma janela de amigo do controle TrackBar em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="f1621-106">Retrieves the handle to a trackbar control buddy window at a given location.</span></span> <span data-ttu-id="f1621-107">O local especificado é relativo à orientação do controle (horizontal ou vertical).</span><span class="sxs-lookup"><span data-stu-id="f1621-107">The specified location is relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="f1621-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1621-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1621-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1621-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1621-110">Valor que indica qual identificador de janela de amigo será recuperado, por local relativo.</span><span class="sxs-lookup"><span data-stu-id="f1621-110">Value indicating which buddy window handle will be retrieved, by relative location.</span></span> <span data-ttu-id="f1621-111">Este valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f1621-111">This value can be one of the following:</span></span>



| <span data-ttu-id="f1621-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f1621-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="f1621-113">Significado</span><span class="sxs-lookup"><span data-stu-id="f1621-113">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="f1621-114"><dt>VERDADEIRO \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f1621-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="f1621-115">Recupera o identificador para o amigo à esquerda do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f1621-115">Retrieves the handle to the buddy to the left of the trackbar.</span></span> <span data-ttu-id="f1621-116">Se o controle TrackBar usar o [**estilo \_ vertical do TBS**](trackbar-control-styles.md) , a mensagem recuperará o colega acima do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f1621-116">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy above the trackbar.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="f1621-117"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f1621-117"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="f1621-118">Recupera o identificador para o amigo à direita do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f1621-118">Retrieves the handle to the buddy to the right of the trackbar.</span></span> <span data-ttu-id="f1621-119">Se o controle TrackBar usar o [**estilo \_ vertical do TBS**](trackbar-control-styles.md) , a mensagem recuperará o colega abaixo do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f1621-119">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy below the trackbar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f1621-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1621-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f1621-121">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f1621-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1621-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1621-122">Return value</span></span>

<span data-ttu-id="f1621-123">Retorna o identificador para a janela Buddy no local especificado por *wParam* ou **NULL** se não existir nenhuma janela Buddy nesse local.</span><span class="sxs-lookup"><span data-stu-id="f1621-123">Returns the handle to the buddy window at the location specified by *wParam*, or **NULL** if no buddy window exists at that location.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1621-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1621-124">Requirements</span></span>



| <span data-ttu-id="f1621-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1621-125">Requirement</span></span> | <span data-ttu-id="f1621-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f1621-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1621-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1621-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f1621-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1621-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1621-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1621-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f1621-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f1621-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1621-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1621-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1621-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1621-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





