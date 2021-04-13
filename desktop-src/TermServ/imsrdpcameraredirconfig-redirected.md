---
title: Propriedade IMsRdpCameraRedirConfig Redirected
description: Especifica se a câmera é redirecionada ou não.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade redirecionada
- Propriedade redirecionada Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfig
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfig, Propriedade redirecionada
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: f81dc643f7911029df088bbb692d7c8c06fddac4
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104456333"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a><span data-ttu-id="0cd68-106">IMsRdpCameraRedirConfig:: Propriedade redirecionada</span><span class="sxs-lookup"><span data-stu-id="0cd68-106">IMsRdpCameraRedirConfig::Redirected property</span></span>

<span data-ttu-id="0cd68-107">Especifica se a câmera é redirecionada ou não.</span><span class="sxs-lookup"><span data-stu-id="0cd68-107">Specifies whether or not the camera is redirected.</span></span>

<span data-ttu-id="0cd68-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0cd68-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd68-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cd68-109">Syntax</span></span>

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a><span data-ttu-id="0cd68-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0cd68-110">Property value</span></span>

<span data-ttu-id="0cd68-111">Um valor que especifica se a câmera é redirecionada ou não.</span><span class="sxs-lookup"><span data-stu-id="0cd68-111">A value that specifies whether or not the camera is redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cd68-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cd68-112">Requirements</span></span>

| <span data-ttu-id="0cd68-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cd68-113">Requirement</span></span> | <span data-ttu-id="0cd68-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0cd68-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="0cd68-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cd68-115">Minimum supported client</span></span>| <span data-ttu-id="0cd68-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="0cd68-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="0cd68-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0cd68-117">Type library</span></span>            | <span data-ttu-id="0cd68-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0cd68-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="0cd68-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0cd68-119">DLL</span></span>                  | <span data-ttu-id="0cd68-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0cd68-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="0cd68-121">IID</span><span class="sxs-lookup"><span data-stu-id="0cd68-121">IID</span></span>                      | <span data-ttu-id="0cd68-122">IID \_ IMsRdpCameraRedirConfig é definido como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="0cd68-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="0cd68-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cd68-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cd68-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="0cd68-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>