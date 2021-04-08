---
title: Propriedade IMsRdpCameraRedirConfigCollection EncodeVideo
description: Especifica se o fluxo de vídeo é ou não codificado em H. 264.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade EncodeVideo
- Propriedade EncodeVideo Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection, Propriedade EncodeVideo
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6b2994f4db3de04f339bb242120b6c63cd2e0c7b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104087195"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a><span data-ttu-id="e634c-106">Propriedade IMsRdpCameraRedirConfigCollection:: EncodeVideo</span><span class="sxs-lookup"><span data-stu-id="e634c-106">IMsRdpCameraRedirConfigCollection::EncodeVideo property</span></span>

<span data-ttu-id="e634c-107">Especifica se o fluxo de vídeo é ou não codificado em H. 264.</span><span class="sxs-lookup"><span data-stu-id="e634c-107">Specifies whether or not the video stream is H.264 encoded.</span></span>

<span data-ttu-id="e634c-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e634c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e634c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e634c-109">Syntax</span></span>

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a><span data-ttu-id="e634c-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e634c-110">Property value</span></span>

<span data-ttu-id="e634c-111">Um valor que indica se o fluxo de vídeo é de H. 264 codificado.</span><span class="sxs-lookup"><span data-stu-id="e634c-111">A value that indicates whether or not the video stream is H.264 encoded.</span></span>

## <a name="requirements"></a><span data-ttu-id="e634c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e634c-112">Requirements</span></span>

| <span data-ttu-id="e634c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e634c-113">Requirement</span></span> | <span data-ttu-id="e634c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e634c-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="e634c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e634c-115">Minimum supported client</span></span>| <span data-ttu-id="e634c-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="e634c-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="e634c-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e634c-117">Type library</span></span>            | <span data-ttu-id="e634c-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e634c-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="e634c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e634c-119">DLL</span></span>                  | <span data-ttu-id="e634c-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e634c-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="e634c-121">IID</span><span class="sxs-lookup"><span data-stu-id="e634c-121">IID</span></span>                      | <span data-ttu-id="e634c-122">IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="e634c-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="e634c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e634c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e634c-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="e634c-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>