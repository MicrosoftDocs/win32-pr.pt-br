---
title: Propriedade IMsRdpCameraRedirConfigCollection EncodingQuality
description: Especifica a qualidade de codificação (taxa de bits).
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade EncodingQuality
- Propriedade EncodingQuality Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection, Propriedade EncodingQuality
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104456329"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a><span data-ttu-id="9be78-106">Propriedade IMsRdpCameraRedirConfigCollection:: EncodingQuality</span><span class="sxs-lookup"><span data-stu-id="9be78-106">IMsRdpCameraRedirConfigCollection::EncodingQuality property</span></span>

<span data-ttu-id="9be78-107">Especifica a qualidade de codificação (taxa de bits).</span><span class="sxs-lookup"><span data-stu-id="9be78-107">Specifies the encoding quality (bit rate).</span></span>

<span data-ttu-id="9be78-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9be78-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be78-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9be78-109">Syntax</span></span>

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a><span data-ttu-id="9be78-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9be78-110">Property value</span></span>

<span data-ttu-id="9be78-111">Um dos seguintes valores de enumeração **CameraRedirEncodingQuality** que especifica a qualidade de codificação (taxa de bits).</span><span class="sxs-lookup"><span data-stu-id="9be78-111">One of the following **CameraRedirEncodingQuality** enum values that specifies the encoding quality (bit rate).</span></span>

| <span data-ttu-id="9be78-112">Nome do membro de enumeração</span><span class="sxs-lookup"><span data-stu-id="9be78-112">Enum member name</span></span> | <span data-ttu-id="9be78-113">Valor</span><span class="sxs-lookup"><span data-stu-id="9be78-113">Value</span></span> |
|-----------------|--------|
| <span data-ttu-id="9be78-114">encodingQualityLow</span><span class="sxs-lookup"><span data-stu-id="9be78-114">encodingQualityLow</span></span> | <span data-ttu-id="9be78-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="9be78-115">0x0000</span></span> |
| <span data-ttu-id="9be78-116">encodingQualityMedium</span><span class="sxs-lookup"><span data-stu-id="9be78-116">encodingQualityMedium</span></span> | <span data-ttu-id="9be78-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="9be78-117">0x0001</span></span> |
| <span data-ttu-id="9be78-118">encodingQualityHigh</span><span class="sxs-lookup"><span data-stu-id="9be78-118">encodingQualityHigh</span></span> | <span data-ttu-id="9be78-119">0x0002</span><span class="sxs-lookup"><span data-stu-id="9be78-119">0x0002</span></span> |

## <a name="requirements"></a><span data-ttu-id="9be78-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9be78-120">Requirements</span></span>

| <span data-ttu-id="9be78-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9be78-121">Requirement</span></span> | <span data-ttu-id="9be78-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9be78-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="9be78-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9be78-123">Minimum supported client</span></span>| <span data-ttu-id="9be78-124">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="9be78-124">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="9be78-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9be78-125">Type library</span></span>            | <span data-ttu-id="9be78-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9be78-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="9be78-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9be78-127">DLL</span></span>                  | <span data-ttu-id="9be78-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9be78-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="9be78-129">IID</span><span class="sxs-lookup"><span data-stu-id="9be78-129">IID</span></span>                      | <span data-ttu-id="9be78-130">IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="9be78-130">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="9be78-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9be78-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be78-132">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="9be78-132">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>