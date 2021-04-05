---
title: Mensagem de BCM_SETIMAGELIST (commctrl. h)
description: Atribui uma lista de imagens a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetImageList do botão.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- Controles de BCM_SETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009270"
---
# <a name="bcm_setimagelist-message"></a><span data-ttu-id="2ca02-105">Mensagem do BCM \_ SETimagelist</span><span class="sxs-lookup"><span data-stu-id="2ca02-105">BCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="2ca02-106">Atribui uma lista de imagens a um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="2ca02-106">Assigns an image list to a button control.</span></span> <span data-ttu-id="2ca02-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetImageList do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="2ca02-107">You can send this message explicitly or use the [**Button\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ca02-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ca02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ca02-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ca02-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ca02-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2ca02-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2ca02-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ca02-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ca02-112">Um ponteiro para uma estrutura de [**botão \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contém informações da lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="2ca02-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ca02-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ca02-113">Return value</span></span>

<span data-ttu-id="2ca02-114">Se a mensagem tiver sucesso, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="2ca02-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="2ca02-115">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="2ca02-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ca02-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ca02-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2ca02-117">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="2ca02-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2ca02-118">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2ca02-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="2ca02-119">A lista de imagens referenciada no membro **himl** da estrutura de [**botão \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) deve conter uma única imagem a ser usada para todos os Estados ou imagens individuais para cada Estado.</span><span class="sxs-lookup"><span data-stu-id="2ca02-119">The image list referred to in the **himl** member of the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure should contain either a single image to be used for all states or individual images for each state.</span></span> <span data-ttu-id="2ca02-120">Os Estados a seguir são definidos em vssym32. h.</span><span class="sxs-lookup"><span data-stu-id="2ca02-120">The following states are defined in vssym32.h.</span></span>

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

<span data-ttu-id="2ca02-121">Observe que o PBS \_ STYLUSHOT é usado somente em computadores tablet.</span><span class="sxs-lookup"><span data-stu-id="2ca02-121">Note that PBS\_STYLUSHOT is used only on tablet computers.</span></span>

<span data-ttu-id="2ca02-122">Cada valor é um índice para a imagem apropriada na lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="2ca02-122">Each value is an index to the appropriate image in the image list.</span></span> <span data-ttu-id="2ca02-123">Se apenas uma imagem estiver presente, ela será usada para todos os Estados.</span><span class="sxs-lookup"><span data-stu-id="2ca02-123">If only one image is present, it is used for all states.</span></span> <span data-ttu-id="2ca02-124">Se a lista de imagens contiver mais de uma imagem, cada índice corresponderá a um estado do botão.</span><span class="sxs-lookup"><span data-stu-id="2ca02-124">If the image list contains more than one image, each index corresponds to one state of the button.</span></span> <span data-ttu-id="2ca02-125">Se uma imagem não for fornecida para cada Estado, nada será desenhado para esses Estados sem imagens.</span><span class="sxs-lookup"><span data-stu-id="2ca02-125">If an image is not provided for each state, nothing is drawn for those states without images.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca02-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca02-126">Requirements</span></span>



| <span data-ttu-id="2ca02-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca02-127">Requirement</span></span> | <span data-ttu-id="2ca02-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2ca02-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca02-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca02-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca02-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ca02-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ca02-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ca02-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca02-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ca02-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ca02-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ca02-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ca02-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca02-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





