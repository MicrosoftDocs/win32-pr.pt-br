---
title: Mensagem de BCM_GETIMAGELIST (commctrl. h)
description: Obtém a estrutura de IMAGELIST do botão \_ que descreve a lista de imagens atribuída a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetImageList do botão.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- Controles de BCM_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455239"
---
# <a name="bcm_getimagelist-message"></a><span data-ttu-id="ea148-105">Mensagem do BCM \_ GETimagelist</span><span class="sxs-lookup"><span data-stu-id="ea148-105">BCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="ea148-106">Obtém a estrutura de [**\_ IMAGELIST do botão**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que descreve a lista de imagens atribuída a um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="ea148-106">Gets the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that describes the image list assigned to a button control.</span></span> <span data-ttu-id="ea148-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetImageList do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="ea148-107">You can send this message explicitly or use the [**Button\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea148-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea148-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea148-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea148-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea148-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ea148-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ea148-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea148-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea148-112">Um ponteiro para uma estrutura de [**botão \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contém informações da lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="ea148-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea148-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea148-113">Return value</span></span>

<span data-ttu-id="ea148-114">Se a mensagem tiver sucesso, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="ea148-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="ea148-115">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="ea148-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea148-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea148-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea148-117">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="ea148-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ea148-118">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ea148-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea148-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea148-119">Requirements</span></span>



| <span data-ttu-id="ea148-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea148-120">Requirement</span></span> | <span data-ttu-id="ea148-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ea148-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea148-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea148-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea148-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea148-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea148-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea148-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea148-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea148-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea148-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea148-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea148-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea148-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





