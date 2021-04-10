---
description: Especifica os sinalizadores de associação a serem usados ao alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: Atributo MF_SA_D3D11_BINDFLAGS (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296816"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a><span data-ttu-id="d63b2-103">\_Atributo MF SA \_ D3D11 \_ BINDFLAGS</span><span class="sxs-lookup"><span data-stu-id="d63b2-103">MF\_SA\_D3D11\_BINDFLAGS attribute</span></span>

<span data-ttu-id="d63b2-104">Especifica os sinalizadores de associação a serem usados ao alocar superfícies do Microsoft Direct3D 11 para exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="d63b2-104">Specifies the binding flags to use when allocating Microsoft Direct3D 11 surfaces for media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="d63b2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d63b2-105">Data type</span></span>

<span data-ttu-id="d63b2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d63b2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d63b2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d63b2-107">Remarks</span></span>

<span data-ttu-id="d63b2-108">O valor desse atributo é um **ou** bit a bit de sinalizadores de [**\_ \_ sinalizador de ligação D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="d63b2-108">The value of this attribute is a bitwise **OR** of [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) flags.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="d63b2-109">Transformações de Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d63b2-109">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="d63b2-110">Nesse contexto, o atributo se aplica somente quando a Microsoft Media Foundation transformação (MFT) retorna **true** para o atributo [MF \_ SA \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="d63b2-110">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="d63b2-111">Se uma MFT der suporte ao Direct3D 11, esse atributo fornecerá uma dica para o MFT ao alocar superfícies do Microsoft Direct3D para saída.</span><span class="sxs-lookup"><span data-stu-id="d63b2-111">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="d63b2-112">Defina o atributo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d63b2-112">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="d63b2-113">Chame [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) para obter o repositório de atributos de MFT.</span><span class="sxs-lookup"><span data-stu-id="d63b2-113">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="d63b2-114">Chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d63b2-114">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="d63b2-115">O pipeline de Media Foundation define o atributo antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="d63b2-115">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="d63b2-116">O MFT deve tentar honrar a configuração ao alocar superfícies.</span><span class="sxs-lookup"><span data-stu-id="d63b2-116">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="d63b2-117">Se isso não for possível, o MFT poderá ignorar o atributo, em vez de falhar a alocação.</span><span class="sxs-lookup"><span data-stu-id="d63b2-117">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="d63b2-118">Além disso, se o MFT exigir superfícies de Direct3D para entrada, ele poderá expor esse atributo como uma dica de como as superfícies de entrada devem ser alocadas.</span><span class="sxs-lookup"><span data-stu-id="d63b2-118">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="d63b2-119">Consulte o atributo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d63b2-119">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="d63b2-120">Chame [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) para obter os atributos de fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="d63b2-120">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="d63b2-121">Chamar [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d63b2-121">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="d63b2-122">Exemplo de alocador</span><span class="sxs-lookup"><span data-stu-id="d63b2-122">Sample Allocator</span></span>

<span data-ttu-id="d63b2-123">Esse atributo pode ser definido no exemplo de alocador de vídeo, no método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="d63b2-123">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d63b2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d63b2-124">Requirements</span></span>



| <span data-ttu-id="d63b2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d63b2-125">Requirement</span></span> | <span data-ttu-id="d63b2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d63b2-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d63b2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d63b2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d63b2-128">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d63b2-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d63b2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d63b2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d63b2-130">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d63b2-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d63b2-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d63b2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d63b2-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="d63b2-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d63b2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d63b2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63b2-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d63b2-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
