---
description: Uma solicitação assíncrona para carregar dados de histograma.
MS-HAID: vspixengine.IPixEngine5\_LoadHistogramAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5:: LoadHistogramAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A23CB3E0-B299-40FD-899E-9FE6E9177551
api_name:
- IPixEngine5.LoadHistogramAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c7128743c2086c0ddc2875c493dac98617986a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105763082"
---
# <a name="span-idvspixengineipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadhistogramasync-method"></a><span data-ttu-id="892ca-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5:: LoadHistogramAsync</span><span class="sxs-lookup"><span data-stu-id="892ca-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadHistogramAsync method</span></span>

<span data-ttu-id="892ca-104">Uma solicitação assíncrona para carregar dados de histograma.</span><span class="sxs-lookup"><span data-stu-id="892ca-104">An asynchronous request to load histogram data.</span></span>

## <a name="syntax"></a><span data-ttu-id="892ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="892ca-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="892ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="892ca-106">Parameters</span></span>

<span data-ttu-id="892ca-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="892ca-107">*textureId* </span></span>  
<span data-ttu-id="892ca-108">A ID da textura para a qual carregar dados de histograma.</span><span class="sxs-lookup"><span data-stu-id="892ca-108">The ID of the texture to load histogram data for.</span></span>

<span data-ttu-id="892ca-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="892ca-109">*sliceIndex* </span></span>  
<span data-ttu-id="892ca-110">O índice da fatia para a qual carregar dados de histograma.</span><span class="sxs-lookup"><span data-stu-id="892ca-110">The index of the slice to load histogram data for.</span></span>

<span data-ttu-id="892ca-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="892ca-111">*formatOverride* </span></span>  
<span data-ttu-id="892ca-112">Especifica a substituição do formato.</span><span class="sxs-lookup"><span data-stu-id="892ca-112">Specifies the format override.</span></span>

<span data-ttu-id="892ca-113">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="892ca-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="892ca-114">Uma cadeia de caracteres COM que contém o nome do arquivo de dados de histograma.</span><span class="sxs-lookup"><span data-stu-id="892ca-114">A COM string containing the name of the histogram data file.</span></span>

<span data-ttu-id="892ca-115">*retornos* </span><span class="sxs-lookup"><span data-stu-id="892ca-115">*callbacks* </span></span>  
<span data-ttu-id="892ca-116">O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="892ca-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="892ca-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="892ca-117">*requestCookie* </span></span>  
<span data-ttu-id="892ca-118">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="892ca-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="892ca-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="892ca-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="892ca-120">Não usado.</span><span class="sxs-lookup"><span data-stu-id="892ca-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="892ca-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="892ca-121">Return value</span></span>

<span data-ttu-id="892ca-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="892ca-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="892ca-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="892ca-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="892ca-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="892ca-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="892ca-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="892ca-125">Header</span></span></p></td><td><span data-ttu-id="892ca-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="892ca-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="892ca-127"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="892ca-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="892ca-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="892ca-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
