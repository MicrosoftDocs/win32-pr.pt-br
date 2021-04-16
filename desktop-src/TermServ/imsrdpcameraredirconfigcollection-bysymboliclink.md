---
title: Propriedade IMsRdpCameraRedirConfigCollection BySymbolicLink
description: Retorna um objeto IMsRdpCameraRedirConfig da coleção que corresponde ao link simbólico fornecido da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BySymbolicLink
- Propriedade BySymbolicLink Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection, Propriedade BySymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105794644"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a><span data-ttu-id="8cfd4-106">IMsRdpCameraRedirConfigCollection::. Propriedade BySymbolicLink</span><span class="sxs-lookup"><span data-stu-id="8cfd4-106">IMsRdpCameraRedirConfigCollection::.BySymbolicLink property</span></span>

<span data-ttu-id="8cfd4-107">Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde ao link simbólico fornecido da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.</span><span class="sxs-lookup"><span data-stu-id="8cfd4-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="8cfd4-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8cfd4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cfd4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cfd4-109">Syntax</span></span>

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="8cfd4-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8cfd4-110">Property value</span></span>

<span data-ttu-id="8cfd4-111">O objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde ao link simbólico especificado.</span><span class="sxs-lookup"><span data-stu-id="8cfd4-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified symbolic link.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfd4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cfd4-112">Requirements</span></span>

| <span data-ttu-id="8cfd4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cfd4-113">Requirement</span></span> | <span data-ttu-id="8cfd4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfd4-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="8cfd4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cfd4-115">Minimum supported client</span></span>| <span data-ttu-id="8cfd4-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="8cfd4-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="8cfd4-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8cfd4-117">Type library</span></span>            | <span data-ttu-id="8cfd4-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="8cfd4-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="8cfd4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8cfd4-119">DLL</span></span>                  | <span data-ttu-id="8cfd4-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="8cfd4-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="8cfd4-121">IID</span><span class="sxs-lookup"><span data-stu-id="8cfd4-121">IID</span></span>                      | <span data-ttu-id="8cfd4-122">IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="8cfd4-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="8cfd4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cfd4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cfd4-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="8cfd4-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>