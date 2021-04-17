---
title: Propriedade IMsRdpCameraRedirConfigCollection ByIndex
description: Retorna um objeto IMsRdpCameraRedirConfig por seu índice na coleção.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ByIndex
- Propriedade ByIndex Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection, Propriedade ByIndex
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 68c179023e93295ee846da22357d5f8efb75b15c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105794643"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a><span data-ttu-id="0df2f-106">Propriedade IMsRdpCameraRedirConfigCollection:: ByIndex</span><span class="sxs-lookup"><span data-stu-id="0df2f-106">IMsRdpCameraRedirConfigCollection::ByIndex property</span></span>

<span data-ttu-id="0df2f-107">Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por seu índice na coleção.</span><span class="sxs-lookup"><span data-stu-id="0df2f-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>

<span data-ttu-id="0df2f-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="0df2f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df2f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0df2f-109">Syntax</span></span>

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="0df2f-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0df2f-110">Property value</span></span>

<span data-ttu-id="0df2f-111">O objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="0df2f-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified index.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df2f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0df2f-112">Requirements</span></span>

| <span data-ttu-id="0df2f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0df2f-113">Requirement</span></span> | <span data-ttu-id="0df2f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0df2f-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="0df2f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0df2f-115">Minimum supported client</span></span>| <span data-ttu-id="0df2f-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="0df2f-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="0df2f-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0df2f-117">Type library</span></span>            | <span data-ttu-id="0df2f-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0df2f-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="0df2f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0df2f-119">DLL</span></span>                  | <span data-ttu-id="0df2f-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0df2f-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="0df2f-121">IID</span><span class="sxs-lookup"><span data-stu-id="0df2f-121">IID</span></span>                      | <span data-ttu-id="0df2f-122">IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="0df2f-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="0df2f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0df2f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df2f-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="0df2f-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>