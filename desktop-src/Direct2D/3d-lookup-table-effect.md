---
title: efeito de tabela de pesquisa 3D
description: Uma tabela de pesquisa 3D é um efeito de uso geral que é usado para encapsular qualquer efeito de imagem de 1 1 ao pré-testar previamente como o efeito mapeia entradas para saídas para um subconjunto de todos os valores de entrada.
ms.assetid: 2f0b4b6d-f371-101c-918a-bf564778e593
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0c6c5df1aa873d3458345d77a46f6f3fdae40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824834"
---
# <a name="3d-lookup-table-effect"></a><span data-ttu-id="53695-103">efeito de tabela de pesquisa 3D</span><span class="sxs-lookup"><span data-stu-id="53695-103">3D lookup table effect</span></span>

<span data-ttu-id="53695-104">Uma tabela de pesquisa 3D é um efeito de uso geral que é usado para encapsular qualquer efeito de imagem de 1:1 ao pré-testar previamente como o efeito mapeia entradas para saídas para um subconjunto de todos os valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="53695-104">A 3D look-up table is a general-purpose effect that is used to encapsulate any 1:1 imaging effect by pre-computing how the effect maps inputs to outputs for a subset of all input values.</span></span>

<span data-ttu-id="53695-105">O efeito da tabela de pesquisa 3D (LUT) modifica uma imagem de entrada usando o valor de cor RGB da imagem para indexar uma textura 3D, em que a textura contém um valor de saída preputado de um pipeline de efeito arbitrário.</span><span class="sxs-lookup"><span data-stu-id="53695-105">The 3D Lookup Table (LUT) effect modifies an input image by using the image's RGB color value to index a 3D texture, where the texture contains a precomputed output value of an arbitrary effect pipeline.</span></span>

<span data-ttu-id="53695-106">O LUT 3D deve ser carregado em um recurso de textura de GPU para ser renderizado, e isso pode ser caro dependendo do tamanho da textura e dos recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53695-106">The 3D LUT must be loaded into a GPU texture resource in order to be rendered, and this can be expensive depending on the size of the texture and the device capabilities.</span></span> <span data-ttu-id="53695-107">Os desenvolvedores de aplicativos podem especificar quando pagar esse custo usando o recurso [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D.</span><span class="sxs-lookup"><span data-stu-id="53695-107">Application developers can specify when to pay this cost using the [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D resource.</span></span> <span data-ttu-id="53695-108">**ID2D1LookupTable3D** tem os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="53695-108">**ID2D1LookupTable3D** has the following attributes:</span></span>

-   <span data-ttu-id="53695-109">Fornece uma representação abstrata do recurso de GPU do 3D LUT.</span><span class="sxs-lookup"><span data-stu-id="53695-109">Provides an abstracted representation of 3D LUT's GPU resource.</span></span>
-   <span data-ttu-id="53695-110">Dependendo dos recursos do dispositivo, uma textura 2D ou 3D será criada e preenchida com os dados LUT fornecidos.</span><span class="sxs-lookup"><span data-stu-id="53695-110">Depending on the device capabilities, either a 2D or 3D texture will be created and filled with the provided LUT data.</span></span>
-   <span data-ttu-id="53695-111">Pode ser passado para a propriedade do efeito LUT 3D para renderização.</span><span class="sxs-lookup"><span data-stu-id="53695-111">Can be passed to the 3D LUT effect's property for rendering.</span></span>

<span data-ttu-id="53695-112">O CLSID para esse efeito é CLSID \_ D2D1LookupTable3D.</span><span class="sxs-lookup"><span data-stu-id="53695-112">The CLSID for this effect is CLSID\_D2D1LookupTable3D.</span></span>

-   [<span data-ttu-id="53695-113">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="53695-113">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="53695-114">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="53695-114">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="53695-115">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="53695-115">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="53695-116">Requirements</span><span class="sxs-lookup"><span data-stu-id="53695-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="53695-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53695-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="53695-118">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="53695-118">Example image</span></span>

![exemplo de saída de efeito](images/3dlookuptable-effect.png)

## <a name="sample-code"></a><span data-ttu-id="53695-120">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="53695-120">Sample code</span></span>

```cpp
//
    // 1. Generate the lookup table data and create an ID2D1LookupTable3D.
    //
 
    // Create a 16x16x16 LUT of arbitrary data type T.
    UINT extents[] = { 16, 16, 16 };
    UINT cElements = extents[0] * extents[1] * extents[2] * 4;
    UINT cbElements = cElements * formatSize;
 
    // Compute the step size in each direction to vary the RGB 
    // channels uniformly over the range [0, 1]
    float steps[] = 
    { 
        1.0f / static_cast<float>(extents[0] - 1),
        1.0f / static_cast<float>(extents[1] - 1),
        1.0f / static_cast<float>(extents[2] - 1),
    };
 
    CArray<BYTE> lutData;
    IFR(lutData.Resize(cbElements));
 
    T* pData = reinterpret_cast<T *>(lutData.GetData());
    T oneValue = ConvertValue<T>(1.0f);
    
    // Generate the LUT by applying an imaging pipeline to RGB values.
    for (UINT iR = 0; iR < extents[2]; iR++)
    {
        for (UINT iG = 0; iG < extents[1]; iG++)
        {
            for (UINT iB = 0; iB < extents[0]; iB++)
            {
                T outputColor[3];
                ApplyPipeline(iR * steps[2], iG * steps[1], iB * steps[0], &outputColor);
 
                pData[0] = outColor[0];
                pData[1] = outColor[1];
                pData[2] = outColor[2];
 
                // Set opaque alpha in the output
                pData[3] = oneValue;
 
                // Advance the pointer
                pData += sizeof(T) * 4;
            }
        }
    }
    
    // Compute the strides of the LUT data.
    UINT strides[2];
    IFR(UIntMult(sizeof(T) * 4, extents[0], &strides[0]));
    IFR(UIntMult(strides[0], extents[1], &strides[1]));
    
    D2D1_BUFFER_PRECISION precision = GetBufferPrecision<T>();
 
    // Create an ID2D1LookupTable3D from the LUT data.
    CComPtr<ID2D1LookupTable3D> sp3dLut;
    IFR(_spEffectContext1->CreateLookupTable3D(
        precision,
        extents,
        lutData.GetData(),
        lutData.GetCount(),
        strides,
        &sp3dLut
        )); 
 
    //
    // 2. To apply the lookup table to an input image, create a LookupTable3D effect
    //    and pass the ID2D1LookupTable3D to the effect as a property.
    //
 
    // Create a 3D LUT effect to render our LUT.
    CComPtr<ID2D1Effect> sp3dLutEffect;
    IFR(pEffectContext->CreateEffect(CLSID_D2D1LookupTable3D, &sp3dLutEffect)); 
 
    // Set the LUT as a property on the effect.
    IFR(sp3dLutEffect->SetValue(D2D1_LOOKUPTABLE3D_PROP_LUT, _spLut));
```

## <a name="effect-properties"></a><span data-ttu-id="53695-121">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="53695-121">Effect properties</span></span>

<span data-ttu-id="53695-122">As propriedades do efeito da tabela de pesquisa 3D são definidas pela enumeração de [**\_ \_ prop d2d1 LOOKUPTABLE3D**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) .</span><span class="sxs-lookup"><span data-stu-id="53695-122">The properties for the 3D lookup table effect are defined by the [**D2D1\_LOOKUPTABLE3D\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="53695-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53695-123">Requirements</span></span>



| <span data-ttu-id="53695-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="53695-124">Requirement</span></span> | <span data-ttu-id="53695-125">Valor</span><span class="sxs-lookup"><span data-stu-id="53695-125">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="53695-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53695-126">Minimum supported client</span></span> | <span data-ttu-id="53695-127">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="53695-127">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="53695-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53695-128">Minimum supported server</span></span> | <span data-ttu-id="53695-129">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="53695-129">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="53695-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53695-130">Header</span></span>                   | <span data-ttu-id="53695-131">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="53695-131">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="53695-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53695-132">Library</span></span>                  | <span data-ttu-id="53695-133">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="53695-133">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="53695-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53695-134">Related topics</span></span>

* [<span data-ttu-id="53695-135">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="53695-135">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
