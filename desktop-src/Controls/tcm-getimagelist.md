---
title: Mensagem de TCM_GETIMAGELIST (commctrl. h)
description: Recupera a lista de imagens associada a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ GetImageList.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- Controles de TCM_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824713"
---
# <a name="tcm_getimagelist-message"></a><span data-ttu-id="bfc2d-105">Mensagem do TCM \_ GETimagelist</span><span class="sxs-lookup"><span data-stu-id="bfc2d-105">TCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="bfc2d-106">Recupera a lista de imagens associada a um controle guia.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-106">Retrieves the image list associated with a tab control.</span></span> <span data-ttu-id="bfc2d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="bfc2d-107">You can send this message explicitly or by using the [**TabCtrl\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bfc2d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfc2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc2d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfc2d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bfc2d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bfc2d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfc2d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bfc2d-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfc2d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bfc2d-113">Return value</span></span>

<span data-ttu-id="bfc2d-114">Retorna o identificador para a lista de imagens, se for bem-sucedido, ou **NULL** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-114">Returns the handle to the image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfc2d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfc2d-115">Requirements</span></span>



| <span data-ttu-id="bfc2d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfc2d-116">Requirement</span></span> | <span data-ttu-id="bfc2d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bfc2d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc2d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfc2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc2d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfc2d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfc2d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfc2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc2d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bfc2d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfc2d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bfc2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfc2d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc2d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





