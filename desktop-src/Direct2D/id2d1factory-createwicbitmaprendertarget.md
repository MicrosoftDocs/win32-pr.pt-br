---
title: Métodos ID2D1Factory CreateWicBitmapRenderTarget
description: Cria um destino de renderização que é renderizado para um bitmap do Microsoft Windows Imaging Component (WIC).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Métodos CreateWicBitmapRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752923"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a><span data-ttu-id="7481e-104">Métodos ID2D1Factory:: CreateWicBitmapRenderTarget</span><span class="sxs-lookup"><span data-stu-id="7481e-104">ID2D1Factory::CreateWicBitmapRenderTarget methods</span></span>

<span data-ttu-id="7481e-105">Cria um destino de renderização que é renderizado para um bitmap do Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="7481e-105">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7481e-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="7481e-106">Overload list</span></span>



| <span data-ttu-id="7481e-107">Método</span><span class="sxs-lookup"><span data-stu-id="7481e-107">Method</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="7481e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7481e-108">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7481e-109">[**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ renderizar \_ \_ Propriedades \* de destino, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="7481e-109">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES\*,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span></span> | <span data-ttu-id="7481e-110">Cria um destino de renderização que é renderizado para um bitmap do Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="7481e-110">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |
| <span data-ttu-id="7481e-111">[**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ renderizar \_ \_ Propriedades de destino&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="7481e-111">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES&,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span></span>  | <span data-ttu-id="7481e-112">Cria um destino de renderização que é renderizado para um bitmap do Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="7481e-112">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7481e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7481e-113">Remarks</span></span>

<span data-ttu-id="7481e-114">Seu aplicativo deve criar destinos de renderização uma vez e mantê-los durante a vida útil do aplicativo ou até que o erro de [**\_ \_ destino de recriação de D2DERR**](direct2d-error-codes.md) seja recebido.</span><span class="sxs-lookup"><span data-stu-id="7481e-114">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="7481e-115">Quando receber esse erro, você precisará recriar o destino de renderização (e todos os recursos que ele criou).</span><span class="sxs-lookup"><span data-stu-id="7481e-115">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

<span data-ttu-id="7481e-116">**Observação**   Esse método não tem suporte em Windows Phone e falhará quando chamado em um dispositivo com o código de erro 0x8899000b (não há dispositivo de renderização de hardware disponível para esta operação).</span><span class="sxs-lookup"><span data-stu-id="7481e-116">**Note**   This method isn't supported on Windows Phone and will fail when called on a device with error code 0x8899000b ( There is no hardware rendering device available for this operation ).</span></span> <span data-ttu-id="7481e-117">Como o emulador de Windows Phone dá suporte à renderização WARP, esse método falhará quando chamado no emulador com um código de erro diferente, 0x88982f80 (wincodec \_ Err \_ unsupportedpixelformat).</span><span class="sxs-lookup"><span data-stu-id="7481e-117">Because the Windows Phone Emulator supports WARP rendering, this method will fail when called on the emulator with a different error code, 0x88982f80 (wincodec\_err\_unsupportedpixelformat).</span></span>

## <a name="requirements"></a><span data-ttu-id="7481e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7481e-118">Requirements</span></span>



| <span data-ttu-id="7481e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7481e-119">Requirement</span></span> | <span data-ttu-id="7481e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7481e-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7481e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7481e-121">Library</span></span><br/> | <dl> <span data-ttu-id="7481e-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7481e-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="7481e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7481e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="7481e-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7481e-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7481e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7481e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7481e-126">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="7481e-126">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

