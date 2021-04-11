---
description: 'Esta seção contém informações sobre os seguintes tipos enumerados e sinalizadores usados com D3DX.:'
ms.assetid: 8836f350-9edd-4521-b7a3-3aa827394c57
title: Enumerações D3DX (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a34ae9c1b275376343ecab321ab9e7762c59fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164093"
---
# <a name="d3dx-enumerations-direct3d-10-graphics"></a><span data-ttu-id="96491-103">Enumerações D3DX (gráficos do Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="96491-103">D3DX Enumerations (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="96491-104">Esta seção contém informações sobre os seguintes tipos enumerados e sinalizadores usados com D3DX.:</span><span class="sxs-lookup"><span data-stu-id="96491-104">This section contains information about the following enumerated types and flags used with D3DX.:</span></span>



| <span data-ttu-id="96491-105">Enumeração</span><span class="sxs-lookup"><span data-stu-id="96491-105">Enumeration</span></span>                                                       | <span data-ttu-id="96491-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="96491-106">Description</span></span>                                                                                                                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96491-107">**\_Sinalizador de canal D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="96491-107">**D3DX10\_CHANNEL\_FLAG**</span></span>](d3dx10-channel-flag.md)              | <span data-ttu-id="96491-108">Esses sinalizadores são usados por funções que operam em um ou mais canais em uma textura.</span><span class="sxs-lookup"><span data-stu-id="96491-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>                                                                                                  |
| [<span data-ttu-id="96491-109">**\_Otimização de CPU D3DX \_**</span><span class="sxs-lookup"><span data-stu-id="96491-109">**D3DX\_CPU\_OPTIMIZATION**</span></span>](d3dx-cpu-optimization.md)          | <span data-ttu-id="96491-110">Especifica o conjunto de instruções D3DX está atualmente otimizado para.</span><span class="sxs-lookup"><span data-stu-id="96491-110">Specifies the instruction set D3DX is currently optimized for.</span></span>                                                                                                                         |
| [<span data-ttu-id="96491-111">**\_Erro D3DX10**</span><span class="sxs-lookup"><span data-stu-id="96491-111">**D3DX10\_ERR**</span></span>](d3dx10-err.md)                                 | <span data-ttu-id="96491-112">Os erros são representados por valores negativos e não podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="96491-112">Errors are represented by negative values and cannot be combined.</span></span>                                                                                                                      |
| [<span data-ttu-id="96491-113">**\_Sinalizador de filtro D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="96491-113">**D3DX10\_FILTER\_FLAG**</span></span>](d3dx10-filter-flag.md)                | <span data-ttu-id="96491-114">Sinalizadores de filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="96491-114">Texture filtering flags.</span></span>                                                                                                                                                               |
| [<span data-ttu-id="96491-115">**\_Formato de \_ arquivo de imagem D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="96491-115">**D3DX10\_IMAGE\_FILE\_FORMAT**</span></span>](d3dx10-image-file-format.md)   | <span data-ttu-id="96491-116">Descreve os formatos de arquivo de imagem com suporte.</span><span class="sxs-lookup"><span data-stu-id="96491-116">Describes the supported image file formats.</span></span>                                                                                                                                            |
| [<span data-ttu-id="96491-117">**\_Malha D3DX10**</span><span class="sxs-lookup"><span data-stu-id="96491-117">**D3DX10\_MESH**</span></span>](d3dx10-mesh.md)                               | <span data-ttu-id="96491-118">Sinalizadores usados para especificar as opções de criação para uma malha.</span><span class="sxs-lookup"><span data-stu-id="96491-118">Flags used to specify creation options for a mesh.</span></span>                                                                                                                                     |
| [<span data-ttu-id="96491-119">**\_Sinalizadores de \_ descarte de malha D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="96491-119">**D3DX10\_MESH\_DISCARD\_FLAGS**</span></span>](d3dx10-mesh-discard-flags.md) | <span data-ttu-id="96491-120">Especifica quais partes de dados de malha descartar do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96491-120">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="96491-121">Usado com [**ID3DX10Mesh::D iscard**](id3dx10mesh-discard.md).</span><span class="sxs-lookup"><span data-stu-id="96491-121">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>                                                         |
| [<span data-ttu-id="96491-122">**D3DX10 \_ MESHOPT**</span><span class="sxs-lookup"><span data-stu-id="96491-122">**D3DX10\_MESHOPT**</span></span>](d3dx10-meshopt.md)                         | <span data-ttu-id="96491-123">Especifica o tipo de otimização de malha a ser executada.</span><span class="sxs-lookup"><span data-stu-id="96491-123">Specifies the type of mesh optimization to be performed.</span></span>                                                                                                                               |
| [<span data-ttu-id="96491-124">**\_Sinalizador D3DX10 NormalMap \_**</span><span class="sxs-lookup"><span data-stu-id="96491-124">**D3DX10\_NORMALMAP\_FLAG**</span></span>](d3dx10-normalmap-flag.md)          | <span data-ttu-id="96491-125">Esses sinalizadores são usados para controlar como o [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) gera mapas normais.</span><span class="sxs-lookup"><span data-stu-id="96491-125">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="96491-126">Qualquer número desses sinalizadores pode estar ou juntos em qualquer combinação.</span><span class="sxs-lookup"><span data-stu-id="96491-126">Any number of these flags may be OR'd together in any combination.</span></span> |
| [<span data-ttu-id="96491-127">**Sinalizador de D3DX10 \_ Salvar \_ textura \_**</span><span class="sxs-lookup"><span data-stu-id="96491-127">**D3DX10\_SAVE\_TEXTURE\_FLAG**</span></span>](d3dx10-save-texture-flag.md)   | <span data-ttu-id="96491-128">Opções de salvamento de textura.</span><span class="sxs-lookup"><span data-stu-id="96491-128">Texture save options.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="96491-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96491-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96491-130">Referência de D3DX</span><span class="sxs-lookup"><span data-stu-id="96491-130">D3DX Reference</span></span>](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 



