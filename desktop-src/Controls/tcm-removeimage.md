---
title: Mensagem de TCM_REMOVEIMAGE (commctrl. h)
description: Remove uma imagem da lista de imagens de um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ RemoveImage.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- Controles de TCM_REMOVEIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756022"
---
# <a name="tcm_removeimage-message"></a><span data-ttu-id="ea380-105">\_Mensagem REMOVEIMAGE de TCM</span><span class="sxs-lookup"><span data-stu-id="ea380-105">TCM\_REMOVEIMAGE message</span></span>

<span data-ttu-id="ea380-106">Remove uma imagem da lista de imagens de um controle guia.</span><span class="sxs-lookup"><span data-stu-id="ea380-106">Removes an image from a tab control's image list.</span></span> <span data-ttu-id="ea380-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) .</span><span class="sxs-lookup"><span data-stu-id="ea380-107">You can send this message explicitly or by using the [**TabCtrl\_RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea380-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea380-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea380-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea380-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea380-110">Índice da imagem a ser removida.</span><span class="sxs-lookup"><span data-stu-id="ea380-110">Index of the image to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ea380-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea380-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ea380-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ea380-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea380-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea380-113">Return value</span></span>

<span data-ttu-id="ea380-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ea380-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea380-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea380-115">Remarks</span></span>

<span data-ttu-id="ea380-116">O controle guia atualiza o índice de imagem de cada guia, de modo que cada guia permanece associada à mesma imagem que antes.</span><span class="sxs-lookup"><span data-stu-id="ea380-116">The tab control updates each tab's image index, so each tab remains associated with the same image as before.</span></span> <span data-ttu-id="ea380-117">Se uma guia estiver usando a imagem que está sendo removida, a guia será definida como sem imagem.</span><span class="sxs-lookup"><span data-stu-id="ea380-117">If a tab is using the image being removed, the tab will be set to have no image.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea380-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea380-118">Requirements</span></span>



| <span data-ttu-id="ea380-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea380-119">Requirement</span></span> | <span data-ttu-id="ea380-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ea380-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea380-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea380-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea380-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea380-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea380-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea380-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea380-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea380-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea380-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea380-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea380-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea380-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





