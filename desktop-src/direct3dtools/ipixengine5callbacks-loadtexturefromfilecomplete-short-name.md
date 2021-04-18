---
description: Uma função de retorno de chamada usada para notificar o host quando um carregamento de textura for concluído.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5Callbacks:: LoadTextureFromFileComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7fb4c38b733a7e85a237260404b5b253e3eb88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105763977"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span data-ttu-id="79154-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>Método IPixEngine5Callbacks:: LoadTextureFromFileComplete</span><span class="sxs-lookup"><span data-stu-id="79154-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureFromFileComplete method</span></span>

<span data-ttu-id="79154-104">Uma função de retorno de chamada usada para notificar o host quando um carregamento de textura for concluído.</span><span class="sxs-lookup"><span data-stu-id="79154-104">A callback function used to notify the host when a texture load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="79154-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79154-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a><span data-ttu-id="79154-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79154-106">Parameters</span></span>

<span data-ttu-id="79154-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="79154-107">*textureId* </span></span>  
<span data-ttu-id="79154-108">A ID da textura carregada.</span><span class="sxs-lookup"><span data-stu-id="79154-108">The ID of the loaded texture.</span></span>

<span data-ttu-id="79154-109">*textureDesc* </span><span class="sxs-lookup"><span data-stu-id="79154-109">*textureDesc* </span></span>  
<span data-ttu-id="79154-110">O descritor de textura da textura carregada.</span><span class="sxs-lookup"><span data-stu-id="79154-110">The texture descriptor of the loaded texture.</span></span>

<span data-ttu-id="79154-111">*numSlices* </span><span class="sxs-lookup"><span data-stu-id="79154-111">*numSlices* </span></span>  
<span data-ttu-id="79154-112">O número de fatias que a textura tem.</span><span class="sxs-lookup"><span data-stu-id="79154-112">The number of slices the texture has.</span></span>

<span data-ttu-id="79154-113">*Count2 \_ sliceIndicies* </span><span class="sxs-lookup"><span data-stu-id="79154-113">*count2\_sliceIndicies* </span></span>  
<span data-ttu-id="79154-114">As índicos de fatia associadas à textura.</span><span class="sxs-lookup"><span data-stu-id="79154-114">Slice indicies associated with the texture.</span></span>

<span data-ttu-id="79154-115">*Count2 \_ sliceDescriptors* </span><span class="sxs-lookup"><span data-stu-id="79154-115">*count2\_sliceDescriptors* </span></span>  
<span data-ttu-id="79154-116">Descritores para cada fatia.</span><span class="sxs-lookup"><span data-stu-id="79154-116">Descriptors for each slice.</span></span>

<span data-ttu-id="79154-117">*numFormatOverrides* </span><span class="sxs-lookup"><span data-stu-id="79154-117">*numFormatOverrides* </span></span>  
<span data-ttu-id="79154-118">O número de substituições de formato.</span><span class="sxs-lookup"><span data-stu-id="79154-118">The number of format overrides.</span></span>

<span data-ttu-id="79154-119">*count5 \_ formatOverrides* </span><span class="sxs-lookup"><span data-stu-id="79154-119">*count5\_formatOverrides* </span></span>  
<span data-ttu-id="79154-120">O formato substitui.</span><span class="sxs-lookup"><span data-stu-id="79154-120">The format overrides.</span></span>

<span data-ttu-id="79154-121">*histograma* </span><span class="sxs-lookup"><span data-stu-id="79154-121">*histogram* </span></span>  
<span data-ttu-id="79154-122">O endereço dos dados de histograma para a textura carregada.</span><span class="sxs-lookup"><span data-stu-id="79154-122">The address of histogram data for the loaded texture.</span></span>

## <a name="return-value"></a><span data-ttu-id="79154-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79154-123">Return value</span></span>

<span data-ttu-id="79154-124">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="79154-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79154-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="79154-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="79154-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79154-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="79154-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79154-127">Header</span></span></p></td><td><span data-ttu-id="79154-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="79154-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="79154-129"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="79154-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="79154-130">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="79154-130">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
