---
title: Métodos ID2D1DeviceContext2 CreateImageSourceFromWic (D2d1 \_ 3. h)
description: Cria um objeto de origem de imagem de uma origem de bitmap do WIC, ao mesmo tempo em que preenche toda a memória de pixel na origem da imagem. A imagem é carregada e armazenada ao usar uma quantidade mínima de memória.
ms.assetid: af02630d-a9ca-f5b4-6f2a-31a73ef603e5
keywords:
- Métodos CreateImageSourceFromWic Direct2D
topic_type:
- apiref
api_location:
- d2d1_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 20773912886840a185e1b9fc71576f89e9a40fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759577"
---
# <a name="id2d1devicecontext2createimagesourcefromwic-methods"></a><span data-ttu-id="c3524-105">Métodos ID2D1DeviceContext2:: CreateImageSourceFromWic</span><span class="sxs-lookup"><span data-stu-id="c3524-105">ID2D1DeviceContext2::CreateImageSourceFromWic methods</span></span>

<span data-ttu-id="c3524-106">Cria um objeto de origem de imagem de uma origem de bitmap do WIC, ao mesmo tempo em que preenche toda a memória de pixel na origem da imagem.</span><span class="sxs-lookup"><span data-stu-id="c3524-106">Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.</span></span> <span data-ttu-id="c3524-107">A imagem é carregada e armazenada ao usar uma quantidade mínima de memória.</span><span class="sxs-lookup"><span data-stu-id="c3524-107">The image is loaded and stored while using a minimal amount of memory.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c3524-108">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="c3524-108">Overload list</span></span>



| <span data-ttu-id="c3524-109">Método</span><span class="sxs-lookup"><span data-stu-id="c3524-109">Method</span></span>                                                                                                                                                                                       | <span data-ttu-id="c3524-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3524-110">Description</span></span>                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3524-111">[**CreateImageSourceFromWic (IWICBitmapSource \* , \_ Opções de carregamento de fonte de imagem d2d1 \_ \_ \_ , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="c3524-111">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span></span>                   | <span data-ttu-id="c3524-112">Versão do método que permite especificar a origem do bitmap do WIC, o objeto de origem da imagem de saída e as opções de carregamento com o modo alfa padrão.</span><span class="sxs-lookup"><span data-stu-id="c3524-112">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options with default alpha mode.</span></span><br/>   |
| <span data-ttu-id="c3524-113">[**CreateImageSourceFromWic (IWICBitmapSource \* , \_ Opções de carregamento de fonte de imagem d2d1 \_ \_ \_ , \_ modo alfa d2d1 \_ , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="c3524-113">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, D2D1\_ALPHA\_MODE, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span></span> | <span data-ttu-id="c3524-114">Versão do método que permite especificar a origem do bitmap do WIC, o objeto de origem da imagem de saída e as opções de carregamento e o modo alfa.</span><span class="sxs-lookup"><span data-stu-id="c3524-114">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options, and alpha mode.</span></span><br/>           |
| <span data-ttu-id="c3524-115">[**CreateImageSourceFromWic (IWICBitmapSource \* , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="c3524-115">[**CreateImageSourceFromWic (IWICBitmapSource\*, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span></span>                                                          | <span data-ttu-id="c3524-116">Versão do método que permite que você especifique a origem do bitmap do WIC e o objeto de origem da imagem de saída com o opitons de carregamento padrão e o modo alfa.</span><span class="sxs-lookup"><span data-stu-id="c3524-116">Version of the method that allows you to specify the WIC bitmap source and the output image source object with default loading opitons and alpha mode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c3524-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3524-117">Requirements</span></span>



| <span data-ttu-id="c3524-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3524-118">Requirement</span></span> | <span data-ttu-id="c3524-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c3524-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3524-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3524-120">Header</span></span><br/> | <dl> <span data-ttu-id="c3524-121"><dt>D2d1 \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3524-121"><dt>D2d1\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3524-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3524-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3524-123">**ID2D1DeviceContext2**</span><span class="sxs-lookup"><span data-stu-id="c3524-123">**ID2D1DeviceContext2**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2)
</dt> </dl>

<span data-ttu-id="c3524-124">�</span><span class="sxs-lookup"><span data-stu-id="c3524-124">�</span></span>

<span data-ttu-id="c3524-125">�</span><span class="sxs-lookup"><span data-stu-id="c3524-125">�</span></span>
