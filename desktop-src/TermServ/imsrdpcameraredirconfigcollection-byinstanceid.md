---
title: Propriedade IMsRdpCameraRedirConfigCollection ByInstanceId
description: Retorna um objeto IMsRdpCameraRedirConfig da coleção que corresponde à ID de instância especificada.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ByInstanceId
- Propriedade ByInstanceId Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection, Propriedade ByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104456326"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a><span data-ttu-id="391d0-106">Propriedade IMsRdpCameraRedirConfigCollection:: ByInstanceId</span><span class="sxs-lookup"><span data-stu-id="391d0-106">IMsRdpCameraRedirConfigCollection::ByInstanceId property</span></span>

<span data-ttu-id="391d0-107">Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde à ID de instância especificada.</span><span class="sxs-lookup"><span data-stu-id="391d0-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>

<span data-ttu-id="391d0-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="391d0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="391d0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="391d0-109">Syntax</span></span>

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="391d0-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="391d0-110">Property value</span></span>

<span data-ttu-id="391d0-111">O objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde à ID de instância especificada.</span><span class="sxs-lookup"><span data-stu-id="391d0-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified instance ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="391d0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="391d0-112">Requirements</span></span>

| <span data-ttu-id="391d0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="391d0-113">Requirement</span></span> | <span data-ttu-id="391d0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="391d0-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="391d0-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="391d0-115">Minimum supported client</span></span>| <span data-ttu-id="391d0-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="391d0-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="391d0-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="391d0-117">Type library</span></span>            | <span data-ttu-id="391d0-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="391d0-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="391d0-119">DLL</span><span class="sxs-lookup"><span data-stu-id="391d0-119">DLL</span></span>                  | <span data-ttu-id="391d0-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="391d0-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="391d0-121">IID</span><span class="sxs-lookup"><span data-stu-id="391d0-121">IID</span></span>                      | <span data-ttu-id="391d0-122">IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="391d0-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="391d0-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="391d0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391d0-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="391d0-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>