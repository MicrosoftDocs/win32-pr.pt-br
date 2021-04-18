---
title: Propriedade IMsRdpCameraRedirConfig ParentInstanceId
description: Obtém a ID da instância do dispositivo pai da câmera.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ParentInstanceId
- Propriedade ParentInstanceId Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfig
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfig, Propriedade ParentInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105793773"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a><span data-ttu-id="fc550-106">IMsRdpCameraRedirConfig: Propriedade arentInstanceId de:P</span><span class="sxs-lookup"><span data-stu-id="fc550-106">IMsRdpCameraRedirConfig::ParentInstanceId property</span></span>

<span data-ttu-id="fc550-107">Obtém a ID da instância do dispositivo pai da câmera.</span><span class="sxs-lookup"><span data-stu-id="fc550-107">Gets the parent device instance ID of the camera.</span></span>

<span data-ttu-id="fc550-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="fc550-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc550-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc550-109">Syntax</span></span>

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a><span data-ttu-id="fc550-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fc550-110">Property value</span></span>

<span data-ttu-id="fc550-111">A ID da instância do dispositivo pai da câmera.</span><span class="sxs-lookup"><span data-stu-id="fc550-111">The parent device instance ID of the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc550-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc550-112">Requirements</span></span>

| <span data-ttu-id="fc550-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc550-113">Requirement</span></span> | <span data-ttu-id="fc550-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fc550-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="fc550-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc550-115">Minimum supported client</span></span>| <span data-ttu-id="fc550-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="fc550-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="fc550-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fc550-117">Type library</span></span>            | <span data-ttu-id="fc550-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fc550-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="fc550-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fc550-119">DLL</span></span>                  | <span data-ttu-id="fc550-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fc550-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="fc550-121">IID</span><span class="sxs-lookup"><span data-stu-id="fc550-121">IID</span></span>                      | <span data-ttu-id="fc550-122">IID \_ IMsRdpCameraRedirConfig é definido como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="fc550-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="fc550-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc550-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc550-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="fc550-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>