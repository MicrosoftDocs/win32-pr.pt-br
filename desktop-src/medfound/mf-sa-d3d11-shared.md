---
description: Indica ao alocador de exemplo de vídeo para criar texturas como compartilháveis usando o mutex com chave.
ms.assetid: 798CA474-3B1A-4795-81B7-563749197104
title: Atributo MF_SA_D3D11_SHARED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6ecb23a99a732e183bc16942e33bbb4f8e3a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169757"
---
# <a name="mf_sa_d3d11_shared-attribute"></a><span data-ttu-id="d22f6-103">\_ \_ Atributo compartilhado D3D11 do MF SA \_</span><span class="sxs-lookup"><span data-stu-id="d22f6-103">MF\_SA\_D3D11\_SHARED attribute</span></span>

<span data-ttu-id="d22f6-104">Indica ao alocador de exemplo de vídeo para criar texturas como compartilháveis usando o mutex com chave.</span><span class="sxs-lookup"><span data-stu-id="d22f6-104">Indicates to the video sample allocator to create textures as shareable using keyed-mutex.</span></span>

## <a name="data-type"></a><span data-ttu-id="d22f6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d22f6-105">Data type</span></span>

<span data-ttu-id="d22f6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d22f6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d22f6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d22f6-107">Remarks</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="d22f6-108">Exemplo de alocador</span><span class="sxs-lookup"><span data-stu-id="d22f6-108">Sample Allocator</span></span>

<span data-ttu-id="d22f6-109">Esse atributo pode ser definido no exemplo de alocador de vídeo, no método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="d22f6-109">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d22f6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d22f6-110">Requirements</span></span>



| <span data-ttu-id="d22f6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d22f6-111">Requirement</span></span> | <span data-ttu-id="d22f6-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d22f6-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d22f6-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d22f6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d22f6-114">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d22f6-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d22f6-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d22f6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d22f6-116">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d22f6-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d22f6-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d22f6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d22f6-118"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="d22f6-118"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d22f6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d22f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22f6-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d22f6-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d22f6-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span><span class="sxs-lookup"><span data-stu-id="d22f6-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[<span data-ttu-id="d22f6-122">MF \_ SA \_ D3D11 \_ compartilhado \_ sem \_ mutex</span><span class="sxs-lookup"><span data-stu-id="d22f6-122">MF\_SA\_D3D11\_SHARED\_WITHOUT\_MUTEX</span></span>](mf-sa-d3d11-shared-without-mutex.md)
</dt> </dl>

 

 




