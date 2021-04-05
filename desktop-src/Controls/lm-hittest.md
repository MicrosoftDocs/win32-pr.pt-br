---
title: Mensagem de LM_HITTEST (commctrl. h)
description: Determina se o usuário clicou no link especificado.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- Controles de LM_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824172"
---
# <a name="lm_hittest-message"></a><span data-ttu-id="85ca5-104">Mensagem de HITTEST do LM \_</span><span class="sxs-lookup"><span data-stu-id="85ca5-104">LM\_HITTEST message</span></span>

<span data-ttu-id="85ca5-105">Determina se o usuário clicou no link especificado.</span><span class="sxs-lookup"><span data-stu-id="85ca5-105">Determines whether the user clicked the specified link.</span></span>

## <a name="parameters"></a><span data-ttu-id="85ca5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85ca5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ca5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85ca5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="85ca5-108">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="85ca5-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="85ca5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85ca5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="85ca5-110">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> a ser preenchida com informações sobre o link no qual o usuário clicou, caso exista.</span><span class="sxs-lookup"><span data-stu-id="85ca5-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> structure to be filled with information about the link the user clicked, if any exists.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ca5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85ca5-111">Return value</span></span>

<span data-ttu-id="85ca5-112">Retorna **true** se o usuário clicou em um link; caso contrário, retorna **false**.</span><span class="sxs-lookup"><span data-stu-id="85ca5-112">Returns **TRUE** if user clicked on a link, otherwise returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="85ca5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="85ca5-113">Remarks</span></span>

<span data-ttu-id="85ca5-114">Se a mensagem de **\_ HITTEST do LM** for bem sucedido, o sistema preencherá o [**LITEM. iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) e o **LITEM. szID**.</span><span class="sxs-lookup"><span data-stu-id="85ca5-114">If the **LM\_HITTEST** message succeeds, the system fills in [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) and **LITEM.szID**.</span></span> <span data-ttu-id="85ca5-115">Se a mensagem de **\_ HITTEST do LM** falhar, não assuma que todas as informações em **litem** são válidas.</span><span class="sxs-lookup"><span data-stu-id="85ca5-115">If the **LM\_HITTEST** message fails, do not assume that any information in **LITEM** is valid.</span></span>

> [!Note]  
> <span data-ttu-id="85ca5-116">Para usar essa API, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="85ca5-116">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="85ca5-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="85ca5-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85ca5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85ca5-118">Requirements</span></span>



| <span data-ttu-id="85ca5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="85ca5-119">Requirement</span></span> | <span data-ttu-id="85ca5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="85ca5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85ca5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85ca5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="85ca5-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85ca5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85ca5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85ca5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="85ca5-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="85ca5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85ca5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85ca5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="85ca5-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ca5-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





