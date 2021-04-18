---
description: Carrega uma fatia de textura e notifica o asynchrnously do host quando ele é concluído.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureSliceAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5:: LoadTextureSliceAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 520DBB6D-D8F3-451F-942C-BE8428B9ADFF
api_name:
- IPixEngine5.LoadTextureSliceAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 505ccfd6668cbe08b4f62878b5f51e9c20185b41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791569"
---
# <a name="span-idvspixengineipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturesliceasync-method"></a><span data-ttu-id="c926a-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5:: LoadTextureSliceAsync</span><span class="sxs-lookup"><span data-stu-id="c926a-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureSliceAsync method</span></span>

<span data-ttu-id="c926a-104">Carrega uma fatia de textura e notifica o asynchrnously do host quando ele é concluído.</span><span class="sxs-lookup"><span data-stu-id="c926a-104">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c926a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c926a-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="c926a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c926a-106">Parameters</span></span>

<span data-ttu-id="c926a-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="c926a-107">*textureId* </span></span>  
<span data-ttu-id="c926a-108">A ID da textura para a qual carregar a fatia.</span><span class="sxs-lookup"><span data-stu-id="c926a-108">The ID of the texture to load the slice for.</span></span>

<span data-ttu-id="c926a-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="c926a-109">*sliceIndex* </span></span>  
<span data-ttu-id="c926a-110">O índice da fatia a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="c926a-110">The index of the slice to load.</span></span>

<span data-ttu-id="c926a-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="c926a-111">*formatOverride* </span></span>  
<span data-ttu-id="c926a-112">Especifica a substituição do formato.</span><span class="sxs-lookup"><span data-stu-id="c926a-112">Specifies the format override.</span></span>

<span data-ttu-id="c926a-113">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="c926a-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="c926a-114">Uma cadeia de caracteres COM que contém o nome do arquivo de dados de histograma associado à fatia de textura.</span><span class="sxs-lookup"><span data-stu-id="c926a-114">A COM string containing the name of the histogram data file associated with the texture slice.</span></span>

<span data-ttu-id="c926a-115">*retornos* </span><span class="sxs-lookup"><span data-stu-id="c926a-115">*callbacks* </span></span>  
<span data-ttu-id="c926a-116">O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="c926a-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="c926a-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="c926a-117">*requestCookie* </span></span>  
<span data-ttu-id="c926a-118">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="c926a-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="c926a-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="c926a-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="c926a-120">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c926a-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="c926a-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c926a-121">Return value</span></span>

<span data-ttu-id="c926a-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c926a-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c926a-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c926a-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c926a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c926a-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c926a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c926a-125">Header</span></span></p></td><td><span data-ttu-id="c926a-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c926a-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c926a-127"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="c926a-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c926a-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="c926a-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
