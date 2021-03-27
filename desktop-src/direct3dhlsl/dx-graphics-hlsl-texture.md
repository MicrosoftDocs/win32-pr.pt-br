---
title: Tipo de textura
description: Use a sintaxe a seguir para declarar uma variável de textura.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Tipo de textura HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2020
ms.locfileid: "103640269"
---
# <a name="texture-type"></a><span data-ttu-id="a5a7b-104">Tipo de textura</span><span class="sxs-lookup"><span data-stu-id="a5a7b-104">Texture type</span></span>

<span data-ttu-id="a5a7b-105">Use a sintaxe a seguir para declarar uma variável de textura.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-105">Use the following syntax to declare a texture variable.</span></span>

|                |
|----------------|
| <span data-ttu-id="a5a7b-106">**Nome do tipo;**</span><span class="sxs-lookup"><span data-stu-id="a5a7b-106">**Type Name;**</span></span> |

## <a name="parameters"></a><span data-ttu-id="a5a7b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5a7b-107">Parameters</span></span>
| <span data-ttu-id="a5a7b-108">Item</span><span class="sxs-lookup"><span data-stu-id="a5a7b-108">Item</span></span>                                                                                     | <span data-ttu-id="a5a7b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5a7b-109">Description</span></span>                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a7b-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Escreva**</span><span class="sxs-lookup"><span data-stu-id="a5a7b-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/> | <span data-ttu-id="a5a7b-111">Um dos seguintes tipos: Texture (não tipado, para compatibilidade com versões anteriores), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-111">One of the following types: texture (untyped, for backwards compatibility), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span></span> <span data-ttu-id="a5a7b-112">O tamanho do elemento deve caber em quantidades de 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-112">The element size must fit into 4 32-bit quantities.</span></span><br/> |
| <span data-ttu-id="a5a7b-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="a5a7b-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/> | <span data-ttu-id="a5a7b-114">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-114">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                   |
## <a name="remarks"></a><span data-ttu-id="a5a7b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5a7b-115">Remarks</span></span>

<span data-ttu-id="a5a7b-116">Há três partes para usar uma textura.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-116">There are three parts to using a texture.</span></span>

1.  <span data-ttu-id="a5a7b-117">Declarando uma variável de textura.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-117">Declaring a texture variable.</span></span> <span data-ttu-id="a5a7b-118">Isso é feito com a sintaxe mostrada acima.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-118">This is done with the syntax shown above.</span></span> <span data-ttu-id="a5a7b-119">Por exemplo, são declarações válidas.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-119">For example, these are valid declarations.</span></span>

    ```
    texture g_MeshTexture;
    ```

    <span data-ttu-id="a5a7b-120">\- ou –</span><span class="sxs-lookup"><span data-stu-id="a5a7b-120">\- or -</span></span>

    ```
    Texture2D g_MeshTexture;
    ```

2.  <span data-ttu-id="a5a7b-121">Declarando e inicializando um objeto de amostra.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-121">Declaring and initializing a sampler object.</span></span> <span data-ttu-id="a5a7b-122">Isso é feito com uma sintaxe ligeiramente diferente no Direct3D 9 e no Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-122">This is done with slightly different syntax in Direct3D 9 and Direct3D 10.</span></span> <span data-ttu-id="a5a7b-123">Para obter detalhes sobre a sintaxe do objeto de amostra, consulte [tipo de amostra (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a5a7b-123">For details about sampler object syntax, see [Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span></span>
3.  <span data-ttu-id="a5a7b-124">Invocar uma função de textura em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-124">Invoking a texture function in a shader.</span></span>

<span data-ttu-id="a5a7b-125">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="a5a7b-125">Differences between Direct3D 9 and Direct3D 10:</span></span>

<span data-ttu-id="a5a7b-126">O Direct3D 9 usa [funções de textura intrínsecas](dx-graphics-hlsl-intrinsic-functions.md) para executar operações de textura.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-126">Direct3D 9 uses [intrinsic texture functions](dx-graphics-hlsl-intrinsic-functions.md) to perform texture operations.</span></span> <span data-ttu-id="a5a7b-127">Este exemplo é do [exemplo BasicHLSL](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) e usa [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) para executar a amostragem de textura.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-127">This example is from the [BasicHLSL Sample](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) and uses [tex2D(s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) to perform texture sampling.</span></span>

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

<span data-ttu-id="a5a7b-128">O Direct3D 10 usa [objetos de textura de modelo](dx-graphics-hlsl-to-type.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-128">Direct3D 10 uses [templated texture objects](dx-graphics-hlsl-to-type.md) instead.</span></span> <span data-ttu-id="a5a7b-129">Aqui está um exemplo da operação de textura equivalente.</span><span class="sxs-lookup"><span data-stu-id="a5a7b-129">Here is an example of the equivalent texture operation.</span></span>

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a><span data-ttu-id="a5a7b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5a7b-130">See also</span></span>

[<span data-ttu-id="a5a7b-131">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5a7b-131">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
