---
description: Especifica como alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: Atributo MF_SA_D3D11_USAGE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164762"
---
# <a name="mf_sa_d3d11_usage-attribute"></a><span data-ttu-id="de8bb-103">\_Atributo de \_ uso de D3D11 do MF SA \_</span><span class="sxs-lookup"><span data-stu-id="de8bb-103">MF\_SA\_D3D11\_USAGE attribute</span></span>

<span data-ttu-id="de8bb-104">Especifica como alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="de8bb-104">Specifies how to allocate Microsoft Direct3D 11 surfaces for media samples.</span></span> <span data-ttu-id="de8bb-105">O uso reflete diretamente se um exemplo pode ser acessado pela CPU ou pela GPU.</span><span class="sxs-lookup"><span data-stu-id="de8bb-105">The usage directly reflects whether a sample is accessible by the CPU or GPU.</span></span>

## <a name="data-type"></a><span data-ttu-id="de8bb-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="de8bb-106">Data type</span></span>

<span data-ttu-id="de8bb-107">**D3D11 \_ USO** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="de8bb-107">**D3D11\_USAGE** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="de8bb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="de8bb-108">Remarks</span></span>

<span data-ttu-id="de8bb-109">O valor desse atributo é um valor [**de \_ uso de D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .</span><span class="sxs-lookup"><span data-stu-id="de8bb-109">The value of this attribute is a [**D3D11\_USAGE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) value.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="de8bb-110">Transformações de Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de8bb-110">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="de8bb-111">Nesse contexto, o atributo se aplica somente quando a Microsoft Media Foundation transformação (MFT) retorna **true** para o atributo [MF \_ SA \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="de8bb-111">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="de8bb-112">Se uma MFT der suporte ao Direct3D 11, esse atributo fornecerá uma dica para o MFT ao alocar superfícies do Microsoft Direct3D para saída.</span><span class="sxs-lookup"><span data-stu-id="de8bb-112">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="de8bb-113">Defina o atributo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="de8bb-113">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="de8bb-114">Chame [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) para obter o repositório de atributos de MFT.</span><span class="sxs-lookup"><span data-stu-id="de8bb-114">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="de8bb-115">Chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="de8bb-115">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="de8bb-116">O pipeline de Media Foundation define o atributo antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="de8bb-116">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="de8bb-117">O MFT deve tentar honrar a configuração ao alocar superfícies.</span><span class="sxs-lookup"><span data-stu-id="de8bb-117">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="de8bb-118">Se isso não for possível, o MFT poderá ignorar o atributo, em vez de falhar a alocação.</span><span class="sxs-lookup"><span data-stu-id="de8bb-118">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="de8bb-119">Além disso, se o MFT exigir superfícies de Direct3D para entrada, ele poderá expor esse atributo como uma dica de como as superfícies de entrada devem ser alocadas.</span><span class="sxs-lookup"><span data-stu-id="de8bb-119">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="de8bb-120">Consulte o atributo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="de8bb-120">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="de8bb-121">Chame [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) para obter os atributos de fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="de8bb-121">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="de8bb-122">Chamar [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="de8bb-122">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="de8bb-123">Exemplo de alocador</span><span class="sxs-lookup"><span data-stu-id="de8bb-123">Sample Allocator</span></span>

<span data-ttu-id="de8bb-124">Esse atributo pode ser definido no exemplo de alocador de vídeo, no método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="de8bb-124">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="de8bb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de8bb-125">Requirements</span></span>



| <span data-ttu-id="de8bb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="de8bb-126">Requirement</span></span> | <span data-ttu-id="de8bb-127">Valor</span><span class="sxs-lookup"><span data-stu-id="de8bb-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de8bb-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de8bb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="de8bb-129">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="de8bb-129">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="de8bb-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de8bb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="de8bb-131">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="de8bb-131">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="de8bb-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de8bb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="de8bb-133"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="de8bb-133"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de8bb-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="de8bb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8bb-135">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de8bb-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
