---
title: Propriedade IMsRdpCameraRedirConfig SymbolicLink
description: Obtém o link simbólico da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SymbolicLink
- Propriedade SymbolicLink Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfig
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfig, Propriedade SymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103825451"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a><span data-ttu-id="0ee3d-106">Propriedade IMsRdpCameraRedirConfig:: SymbolicLink</span><span class="sxs-lookup"><span data-stu-id="0ee3d-106">IMsRdpCameraRedirConfig::SymbolicLink property</span></span>

<span data-ttu-id="0ee3d-107">Obtém o link simbólico da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.</span><span class="sxs-lookup"><span data-stu-id="0ee3d-107">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="0ee3d-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="0ee3d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee3d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ee3d-109">Syntax</span></span>

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a><span data-ttu-id="0ee3d-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0ee3d-110">Property value</span></span>

<span data-ttu-id="0ee3d-111">O link simbólico da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.</span><span class="sxs-lookup"><span data-stu-id="0ee3d-111">The symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee3d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ee3d-112">Requirements</span></span>

| <span data-ttu-id="0ee3d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ee3d-113">Requirement</span></span> | <span data-ttu-id="0ee3d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0ee3d-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="0ee3d-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ee3d-115">Minimum supported client</span></span>| <span data-ttu-id="0ee3d-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="0ee3d-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="0ee3d-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0ee3d-117">Type library</span></span>            | <span data-ttu-id="0ee3d-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0ee3d-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="0ee3d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0ee3d-119">DLL</span></span>                  | <span data-ttu-id="0ee3d-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0ee3d-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="0ee3d-121">IID</span><span class="sxs-lookup"><span data-stu-id="0ee3d-121">IID</span></span>                      | <span data-ttu-id="0ee3d-122">IID \_ IMsRdpCameraRedirConfig é definido como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="0ee3d-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="0ee3d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ee3d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee3d-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="0ee3d-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>