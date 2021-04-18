---
description: Lê um valor Texel e retorna o resultado para o host asynchrnously.
MS-HAID: vspixengine.IPixEngine5\_ReadTexelValueAsync\_UINT\_PixEngineTextureSliceIndex\_int\_int\_int\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5:: ReadTexelValueAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 28C44D12-383D-4E91-8BB1-12869782533C
api_name:
- IPixEngine5.ReadTexelValueAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ca3510b01038df3b07b3033364902f76f2e05b4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105807932"
---
# <a name="span-idvspixengineipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dwordspanipixengine5readtexelvalueasync-method"></a><span data-ttu-id="d6cb6-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5:: ReadTexelValueAsync</span><span class="sxs-lookup"><span data-stu-id="d6cb6-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::ReadTexelValueAsync method</span></span>

<span data-ttu-id="d6cb6-104">Lê um valor Texel e retorna o resultado para o host asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-104">Reads a texel value and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6cb6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6cb6-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        x,
   int                        y,
   int                        formatOverride,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="d6cb6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6cb6-106">Parameters</span></span>

<span data-ttu-id="d6cb6-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="d6cb6-107">*textureId* </span></span>  
<span data-ttu-id="d6cb6-108">A ID da textura da qual ler o valor de Texel.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-108">The ID of the texture to read the texel value from.</span></span>

<span data-ttu-id="d6cb6-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="d6cb6-109">*sliceIndex* </span></span>  
<span data-ttu-id="d6cb6-110">O índice da fatia dentro da textura da qual ler o valor de Texel.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-110">The index of the slice within the texture to read the texel value from.</span></span>

<span data-ttu-id="d6cb6-111">*w.x.y.* </span><span class="sxs-lookup"><span data-stu-id="d6cb6-111">*x* </span></span>  
<span data-ttu-id="d6cb6-112">A coordenada x Texel para ler.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-112">The x texel coordinate to read.</span></span>

<span data-ttu-id="d6cb6-113">*Iar* </span><span class="sxs-lookup"><span data-stu-id="d6cb6-113">*y* </span></span>  
<span data-ttu-id="d6cb6-114">A coordenada y Texel para ler.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-114">The y texel coordinate to read.</span></span>

<span data-ttu-id="d6cb6-115">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="d6cb6-115">*formatOverride* </span></span>  
<span data-ttu-id="d6cb6-116">A substituição do formato de cor.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-116">The color format override.</span></span>

<span data-ttu-id="d6cb6-117">*retornos* </span><span class="sxs-lookup"><span data-stu-id="d6cb6-117">*callbacks* </span></span>  
<span data-ttu-id="d6cb6-118">O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-118">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="d6cb6-119">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="d6cb6-119">*requestCookie* </span></span>  
<span data-ttu-id="d6cb6-120">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-120">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="d6cb6-121">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="d6cb6-121">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="d6cb6-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-122">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6cb6-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6cb6-123">Return value</span></span>

<span data-ttu-id="d6cb6-124">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6cb6-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6cb6-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6cb6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6cb6-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d6cb6-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6cb6-127">Header</span></span></p></td><td><span data-ttu-id="d6cb6-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d6cb6-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d6cb6-129"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="d6cb6-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d6cb6-130">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="d6cb6-130">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
