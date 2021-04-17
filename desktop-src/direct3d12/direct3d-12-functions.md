---
title: Funções principais (Direct3D 12 Graphics)
description: As funções a seguir são declaradas em d3d12. h.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: 99ec8516634a0a59262df9862e03732c9d6d579a
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "105811695"
---
# <a name="core-functions"></a><span data-ttu-id="964f8-103">Funções de núcleo</span><span class="sxs-lookup"><span data-stu-id="964f8-103">Core functions</span></span>

<span data-ttu-id="964f8-104">As funções a seguir são declaradas em d3d12. h.</span><span class="sxs-lookup"><span data-stu-id="964f8-104">The following functions are declared in d3d12.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="964f8-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="964f8-105">In this section</span></span>

| <span data-ttu-id="964f8-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="964f8-106">Topic</span></span> | <span data-ttu-id="964f8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="964f8-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="964f8-108">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="964f8-108">**D3D12CreateDevice**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | <span data-ttu-id="964f8-109">Cria um dispositivo que representa o adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="964f8-109">Creates a device that represents the display adapter.</span></span> |
| [<span data-ttu-id="964f8-110">**D3D12CreateRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="964f8-110">**D3D12CreateRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | <span data-ttu-id="964f8-111">Desserializa uma assinatura de raiz para que você possa determinar a definição de layout ([**D3D12id da \_ \_ assinatura \_ raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span><span class="sxs-lookup"><span data-stu-id="964f8-111">Deserializes a root signature so you can determine the layout definition ([**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span></span> |
| [<span data-ttu-id="964f8-112">**D3D12CreateVersionedRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="964f8-112">**D3D12CreateVersionedRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | <span data-ttu-id="964f8-113">Gera uma interface que pode retornar a estrutura de dados desserializada, por meio de [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span><span class="sxs-lookup"><span data-stu-id="964f8-113">Generates an interface that can return the deserialized data structure, via [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span></span> |
| [<span data-ttu-id="964f8-114">**D3D12EnableExperimentalFeatures**</span><span class="sxs-lookup"><span data-stu-id="964f8-114">**D3D12EnableExperimentalFeatures**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | <span data-ttu-id="964f8-115">Habilita uma lista de recursos experimentais.</span><span class="sxs-lookup"><span data-stu-id="964f8-115">Enables a list of experimental features.</span></span> |
| [<span data-ttu-id="964f8-116">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="964f8-116">**D3D12GetDebugInterface**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | <span data-ttu-id="964f8-117">Obtém uma interface de depuração.</span><span class="sxs-lookup"><span data-stu-id="964f8-117">Gets a debug interface.</span></span> |
| [<span data-ttu-id="964f8-118">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="964f8-118">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | <span data-ttu-id="964f8-119">Serializa uma versão de assinatura raiz 1,0 que pode ser passada para [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="964f8-119">Serializes a root signature version 1.0 that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |
| [<span data-ttu-id="964f8-120">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="964f8-120">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | <span data-ttu-id="964f8-121">Serializa uma assinatura raiz de qualquer versão que possa ser passada para [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="964f8-121">Serializes a root signature of any version that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="964f8-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="964f8-122">Related topics</span></span>

* [<span data-ttu-id="964f8-123">Referência de núcleo</span><span class="sxs-lookup"><span data-stu-id="964f8-123">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="964f8-124">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="964f8-124">Direct3D 12 reference</span></span>](direct3d-12-reference.md)






