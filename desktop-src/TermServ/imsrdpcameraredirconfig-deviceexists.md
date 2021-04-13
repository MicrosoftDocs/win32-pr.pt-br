---
title: Propriedade IMsRdpCameraRedirConfig DeviceExists
description: Especifica se o dispositivo de câmera existe ou não no momento (ou seja, a câmera está conectada).
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceExists
- Propriedade DeviceExists Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfig
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfig, Propriedade DeviceExists
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 368b2d46e6dfc2c32c0bb294edceda31f8a58f4e
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104456335"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a><span data-ttu-id="f0f09-106">IMsRdpCameraRedirConfig: Propriedade eviceExists de:D</span><span class="sxs-lookup"><span data-stu-id="f0f09-106">IMsRdpCameraRedirConfig::DeviceExists property</span></span>

<span data-ttu-id="f0f09-107">Especifica se o dispositivo de câmera existe ou não no momento (ou seja, a câmera está conectada).</span><span class="sxs-lookup"><span data-stu-id="f0f09-107">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>

<span data-ttu-id="f0f09-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f0f09-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f09-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0f09-109">Syntax</span></span>

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a><span data-ttu-id="f0f09-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f0f09-110">Property value</span></span>

<span data-ttu-id="f0f09-111">Um valor que indica se o dispositivo de câmera existe ou não no momento (ou seja, a câmera está conectada).</span><span class="sxs-lookup"><span data-stu-id="f0f09-111">A value that indicates whether or not the camera device currently exists (that is, the camera is connected).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0f09-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0f09-112">Requirements</span></span>

| <span data-ttu-id="f0f09-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0f09-113">Requirement</span></span> | <span data-ttu-id="f0f09-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f0f09-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f0f09-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0f09-115">Minimum supported client</span></span>| <span data-ttu-id="f0f09-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="f0f09-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f0f09-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f0f09-117">Type library</span></span>            | <span data-ttu-id="f0f09-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f0f09-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f0f09-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f0f09-119">DLL</span></span>                  | <span data-ttu-id="f0f09-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f0f09-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f0f09-121">IID</span><span class="sxs-lookup"><span data-stu-id="f0f09-121">IID</span></span>                      | <span data-ttu-id="f0f09-122">IID \_ IMsRdpCameraRedirConfig é definido como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="f0f09-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="f0f09-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0f09-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0f09-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="f0f09-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>