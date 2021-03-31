---
description: Constantes de intenção de imagem especificam o tipo de dados que a imagem deve representar.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Constantes de intenção de imagem (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921072"
---
# <a name="image-intent-constants"></a><span data-ttu-id="8daf2-103">Constantes da intenção de imagem</span><span class="sxs-lookup"><span data-stu-id="8daf2-103">Image Intent Constants</span></span>

<span data-ttu-id="8daf2-104">Constantes de intenção de imagem especificam o tipo de dados que a imagem deve representar.</span><span class="sxs-lookup"><span data-stu-id="8daf2-104">Image intent constants specify what type of data the image is meant to represent.</span></span> <span data-ttu-id="8daf2-105">A propriedade do scanner de tentativa de propriedade [**\_ atual de IPS \_ \_ WIA**](-wia-wiaitempropscanneritem.md) usa esses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="8daf2-105">The [**WIA\_IPS\_CUR\_INTENT**](-wia-wiaitempropscanneritem.md) scanner property uses these flags.</span></span> <span data-ttu-id="8daf2-106">Para fornecer uma intenção, combine um sinalizador de tipo de imagem pretendido com um sinalizador de tamanho/qualidade pretendido usando o operador OR.</span><span class="sxs-lookup"><span data-stu-id="8daf2-106">To provide an intent, combine an intended image type flag with an intended size/quality flag by using the OR operator.</span></span> <span data-ttu-id="8daf2-107">\_A intenção WIA \_ None não deve ser combinada com nenhum outro sinalizador.</span><span class="sxs-lookup"><span data-stu-id="8daf2-107">WIA\_INTENT\_NONE should not be combined with any other flags.</span></span> <span data-ttu-id="8daf2-108">Observe que uma imagem não pode ser escala de cinza e cor.</span><span class="sxs-lookup"><span data-stu-id="8daf2-108">Note that an image cannot be both grayscale and color.</span></span>

<span data-ttu-id="8daf2-109">Estas são constantes de tentativa de imagem válidas:</span><span class="sxs-lookup"><span data-stu-id="8daf2-109">The following are valid image intent constants:</span></span>



| <span data-ttu-id="8daf2-110">Sinalizadores de tipo de imagem pretendidos</span><span class="sxs-lookup"><span data-stu-id="8daf2-110">Intended image type flags</span></span>           | <span data-ttu-id="8daf2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8daf2-111">Description</span></span>                                  |
|-------------------------------------|----------------------------------------------|
| <span data-ttu-id="8daf2-112">\_intenção WIA \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8daf2-112">WIA\_INTENT\_NONE</span></span>                   | <span data-ttu-id="8daf2-113">Valor padrão.</span><span class="sxs-lookup"><span data-stu-id="8daf2-113">Default value.</span></span> <span data-ttu-id="8daf2-114">Não Predefina nenhuma propriedade.</span><span class="sxs-lookup"><span data-stu-id="8daf2-114">Do not preset any properties.</span></span> |
| <span data-ttu-id="8daf2-115">\_cor do \_ tipo de imagem da intenção WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="8daf2-115">WIA\_INTENT\_IMAGE\_TYPE\_COLOR</span></span>     | <span data-ttu-id="8daf2-116">Propriedades predefinidas para conteúdo de cores.</span><span class="sxs-lookup"><span data-stu-id="8daf2-116">Preset properties for color content.</span></span>         |
| <span data-ttu-id="8daf2-117">\_tipo de imagem da intenção WIA escala de \_ \_ \_ cinza</span><span class="sxs-lookup"><span data-stu-id="8daf2-117">WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE</span></span> | <span data-ttu-id="8daf2-118">Propriedades predefinidas para conteúdo em tons de cinza.</span><span class="sxs-lookup"><span data-stu-id="8daf2-118">Preset properties for grayscale content.</span></span>     |
| <span data-ttu-id="8daf2-119">\_texto do \_ tipo de imagem da intenção WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="8daf2-119">WIA\_INTENT\_IMAGE\_TYPE\_TEXT</span></span>      | <span data-ttu-id="8daf2-120">Propriedades predefinidas para conteúdo de texto.</span><span class="sxs-lookup"><span data-stu-id="8daf2-120">Preset properties for text content.</span></span>          |
| <span data-ttu-id="8daf2-121">\_máscara do \_ tipo de imagem da intenção WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="8daf2-121">WIA\_INTENT\_IMAGE\_TYPE\_MASK</span></span>      | <span data-ttu-id="8daf2-122">Máscara para todos os sinalizadores de tipo de imagem.</span><span class="sxs-lookup"><span data-stu-id="8daf2-122">Mask for all of the image type flags.</span></span>        |



 



| <span data-ttu-id="8daf2-123">Tamanho de imagem pretendido/sinalizadores de qualidade</span><span class="sxs-lookup"><span data-stu-id="8daf2-123">Intended image size/quality flags</span></span> | <span data-ttu-id="8daf2-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="8daf2-124">Description</span></span>                                  |
|-----------------------------------|----------------------------------------------|
| <span data-ttu-id="8daf2-125">\_tamanho de \_ minimização da intenção WIA \_</span><span class="sxs-lookup"><span data-stu-id="8daf2-125">WIA\_INTENT\_MINIMIZE\_SIZE</span></span>       | <span data-ttu-id="8daf2-126">Propriedades predefinidas para minimizar o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="8daf2-126">Preset properties to minimize image size.</span></span>    |
| <span data-ttu-id="8daf2-127">objetivo do WIA \_ \_ maximizar \_ qualidade</span><span class="sxs-lookup"><span data-stu-id="8daf2-127">WIA\_INTENT\_MAXIMIZE\_QUALITY</span></span>    | <span data-ttu-id="8daf2-128">Propriedades predefinidas para maximizar a qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="8daf2-128">Preset properties to maximize image quality.</span></span> |
| <span data-ttu-id="8daf2-129">\_máscara de \_ tamanho de intenção WIA \_</span><span class="sxs-lookup"><span data-stu-id="8daf2-129">WIA\_INTENT\_SIZE\_MASK</span></span>           | <span data-ttu-id="8daf2-130">Máscara para todos os sinalizadores de tamanho/qualidade.</span><span class="sxs-lookup"><span data-stu-id="8daf2-130">Mask for all of the size/quality flags.</span></span>      |
| <span data-ttu-id="8daf2-131">\_ \_ melhor visualização da intenção WIA \_</span><span class="sxs-lookup"><span data-stu-id="8daf2-131">WIA\_INTENT\_BEST\_PREVIEW</span></span>        | <span data-ttu-id="8daf2-132">Especifica a melhor visualização de qualidade.</span><span class="sxs-lookup"><span data-stu-id="8daf2-132">Specifies the best quality preview.</span></span>          |



 

<span data-ttu-id="8daf2-133">A lista a seguir mostra o nome da constante C/C++ seguido pelo nome correspondente entre parênteses que é usado no script.</span><span class="sxs-lookup"><span data-stu-id="8daf2-133">The following list shows the C/C++ constant name followed by the corresponding name in parentheses that is used in scripting.</span></span> <span data-ttu-id="8daf2-134">Os nomes de script são do tipo enumerado WiaIntent.</span><span class="sxs-lookup"><span data-stu-id="8daf2-134">The script names are from the WiaIntent enumerated type.</span></span> <span data-ttu-id="8daf2-135">Observe que nem todas as constantes estão disponíveis por meio de script.</span><span class="sxs-lookup"><span data-stu-id="8daf2-135">Note that not all constants are available through script.</span></span>



| <span data-ttu-id="8daf2-136">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="8daf2-136">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="8daf2-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="8daf2-137">Description</span></span>                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <span data-ttu-id="8daf2-138"><dt>**WIA \_ \_Cor do \_ tipo \_ de imagem da intenção**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8daf2-138"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_COLOR**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="8daf2-139">Propriedades predefinidas para conteúdo de cores.</span><span class="sxs-lookup"><span data-stu-id="8daf2-139">Preset properties for color content.</span></span><br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <span data-ttu-id="8daf2-140"><dt>**WIA \_ Tipo de imagem de intenção \_ \_ tons de \_ cinza**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="8daf2-140"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="8daf2-141">Propriedades predefinidas para conteúdo em tons de cinza.</span><span class="sxs-lookup"><span data-stu-id="8daf2-141">Preset properties for grayscale content.</span></span><br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <span data-ttu-id="8daf2-142"><dt>**WIA \_ Tipo de imagem de intenção \_ \_ \_ texto**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="8daf2-142"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_TEXT**</dt> <dt>0x00000004</dt></span></span> </dl>                | <span data-ttu-id="8daf2-143">Propriedades predefinidas para conteúdo de texto.</span><span class="sxs-lookup"><span data-stu-id="8daf2-143">Preset properties for text content.</span></span><br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <span data-ttu-id="8daf2-144"><dt>**WIA \_ 0x00010000 \_ de \_ tamanho de minimizar intenção**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8daf2-144"><dt>**WIA\_INTENT\_MINIMIZE\_SIZE**</dt> <dt>0x00010000</dt></span></span> </dl>                       | <span data-ttu-id="8daf2-145">Propriedades predefinidas para minimizar o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="8daf2-145">Preset properties to minimize image size.</span></span><br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <span data-ttu-id="8daf2-146"><dt>**WIA \_ INTENÇÃO \_ maximizar \_ qualidade**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="8daf2-146"><dt>**WIA\_INTENT\_MAXIMIZE\_QUALITY**</dt> <dt>0x00020000</dt></span></span> </dl>              | <span data-ttu-id="8daf2-147">Propriedades predefinidas para maximizar a qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="8daf2-147">Preset properties to maximize image quality.</span></span><br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <span data-ttu-id="8daf2-148"><dt>**WIA \_ 0x00040000 de \_ melhor \_ Visualização da intenção**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8daf2-148"><dt>**WIA\_INTENT\_BEST\_PREVIEW**</dt> <dt>0x00040000</dt></span></span> </dl>                          | <span data-ttu-id="8daf2-149">Especifica a melhor visualização de qualidade.</span><span class="sxs-lookup"><span data-stu-id="8daf2-149">Specifies the best quality preview.</span></span><br/>          |



## <a name="requirements"></a><span data-ttu-id="8daf2-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8daf2-150">Requirements</span></span>



| <span data-ttu-id="8daf2-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="8daf2-151">Requirement</span></span> | <span data-ttu-id="8daf2-152">Valor</span><span class="sxs-lookup"><span data-stu-id="8daf2-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8daf2-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8daf2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8daf2-154">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8daf2-154">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8daf2-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8daf2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8daf2-156">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8daf2-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8daf2-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8daf2-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="8daf2-158"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="8daf2-158"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




