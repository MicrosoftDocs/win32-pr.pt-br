---
title: GUIDs de atributo do adaptador de DXCore
description: 'As seguintes GUIDs de atributo de adaptador são declaradas em `dxcore_interface.h` e são usadas com os métodos [IDXCoreAdapterFactory:: createadapterlist](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter:: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) .'
keywords:
- DXCore, atributo de adaptador, GUIDs
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a532552f144dfc21aa5d6a368aecd915d30b40c8
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/31/2021
ms.locfileid: "106098489"
---
# <a name="dxcore-adapter-attribute-guids"></a><span data-ttu-id="0f9b0-104">GUIDs de atributo do adaptador de DXCore</span><span class="sxs-lookup"><span data-stu-id="0f9b0-104">DXCore adapter attribute GUIDs</span></span>

<span data-ttu-id="0f9b0-105">As seguintes GUIDs de atributo de adaptador são declaradas em `dxcore_interface.h` e são usadas com os métodos [IDXCoreAdapterFactory:: createadapterlist](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter:: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) .</span><span class="sxs-lookup"><span data-stu-id="0f9b0-105">The following adapter attribute GUIDs are declared in `dxcore_interface.h`, and are used with the [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) and [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) methods.</span></span> <span data-ttu-id="0f9b0-106">Para qualquer adaptador, um ou mais dos atributos podem ser aplicados.</span><span class="sxs-lookup"><span data-stu-id="0f9b0-106">For any given adapter, one or more of the attributes could apply.</span></span>

| <span data-ttu-id="0f9b0-107">GUID</span><span class="sxs-lookup"><span data-stu-id="0f9b0-107">GUID</span></span> | <span data-ttu-id="0f9b0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0f9b0-108">Value</span></span> |
|-|-|
| <span data-ttu-id="0f9b0-109">`DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`.</span><span class="sxs-lookup"><span data-stu-id="0f9b0-109">`DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`.</span></span> <span data-ttu-id="0f9b0-110">Especifica um adaptador que oferece suporte para uso com as APIs de gráficos do [Direct3D 11](/windows/win32/direct3d11) .</span><span class="sxs-lookup"><span data-stu-id="0f9b0-110">Specifies an adapter that supports being used with the [Direct3D 11](/windows/win32/direct3d11) graphics APIs.</span></span> <span data-ttu-id="0f9b0-111">Nenhuma garantia é feita sobre recursos específicos, nem uma garantia de que o sistema operacional em sua configuração atual dê suporte a essas APIs.</span><span class="sxs-lookup"><span data-stu-id="0f9b0-111">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="0f9b0-112">0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b</span><span class="sxs-lookup"><span data-stu-id="0f9b0-112">0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b</span></span> |
| <span data-ttu-id="0f9b0-113">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`.</span><span class="sxs-lookup"><span data-stu-id="0f9b0-113">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`.</span></span> <span data-ttu-id="0f9b0-114">Especifica um adaptador que oferece suporte para uso com as APIs de gráficos do [Direct3D 12](/windows/win32/direct3d12) .</span><span class="sxs-lookup"><span data-stu-id="0f9b0-114">Specifies an adapter that supports being used with the [Direct3D 12](/windows/win32/direct3d12) graphics APIs.</span></span> <span data-ttu-id="0f9b0-115">Nenhuma garantia é feita sobre recursos específicos, nem uma garantia de que o sistema operacional em sua configuração atual dê suporte a essas APIs.</span><span class="sxs-lookup"><span data-stu-id="0f9b0-115">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="0f9b0-116">0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9e, 0x33, 0x1B, 0x47, 0xB1</span><span class="sxs-lookup"><span data-stu-id="0f9b0-116">0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9e, 0x33, 0x1b, 0x47, 0xb1</span></span> |
| <span data-ttu-id="0f9b0-117">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`.</span><span class="sxs-lookup"><span data-stu-id="0f9b0-117">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`.</span></span> <span data-ttu-id="0f9b0-118">Especifica um adaptador que oferece suporte para uso com as APIs de computação [principal do Direct3D 12](../direct3d12/core-feature-levels.md) .</span><span class="sxs-lookup"><span data-stu-id="0f9b0-118">Specifies an adapter that supports being used with the [Direct3D 12 Core](../direct3d12/core-feature-levels.md) compute APIs.</span></span> <span data-ttu-id="0f9b0-119">Nenhuma garantia é feita sobre recursos específicos, nem uma garantia de que o sistema operacional em sua configuração atual dê suporte a essas APIs.</span><span class="sxs-lookup"><span data-stu-id="0f9b0-119">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="0f9b0-120">0x248e2800, 0xa793, 0x4724, 0xab, 0xAA, 0x23, 0xA6, 0xde, 0x1B, 0xE0, 0x90</span><span class="sxs-lookup"><span data-stu-id="0f9b0-120">0x248e2800, 0xa793, 0x4724, 0xab, 0xaa, 0x23, 0xa6, 0xde, 0x1b, 0xe0, 0x90</span></span> |

## <a name="requirements"></a><span data-ttu-id="0f9b0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f9b0-121">Requirements</span></span>

| <span data-ttu-id="0f9b0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f9b0-122">Requirement</span></span> | <span data-ttu-id="0f9b0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0f9b0-123">Value</span></span> |
|-|-|
| <span data-ttu-id="0f9b0-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f9b0-124">Header</span></span> | <span data-ttu-id="0f9b0-125">dxcore_interface. h</span><span class="sxs-lookup"><span data-stu-id="0f9b0-125">dxcore_interface.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="0f9b0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f9b0-126">See also</span></span>

* [<span data-ttu-id="0f9b0-127">IDXCoreAdapterFactory::CreateAdapterList</span><span class="sxs-lookup"><span data-stu-id="0f9b0-127">IDXCoreAdapterFactory::CreateAdapterList</span></span>](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [<span data-ttu-id="0f9b0-128">IDXCoreAdapter::IsAttributeSupported</span><span class="sxs-lookup"><span data-stu-id="0f9b0-128">IDXCoreAdapter::IsAttributeSupported</span></span>](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [<span data-ttu-id="0f9b0-129">Referência de DXCore</span><span class="sxs-lookup"><span data-stu-id="0f9b0-129">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="0f9b0-130">Usar DXCore para enumerar adaptadores</span><span class="sxs-lookup"><span data-stu-id="0f9b0-130">Using DXCore to enumerate adapters</span></span>](./dxcore-enum-adapters.md)
* [<span data-ttu-id="0f9b0-131">Gráficos do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0f9b0-131">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)
