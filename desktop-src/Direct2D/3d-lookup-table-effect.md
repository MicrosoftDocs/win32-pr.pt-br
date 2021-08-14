---
title: efeito de tabela de pesquisa 3D
description: Uma tabela de pesquisa 3D é um efeito de uso geral que é usado para encapsular qualquer efeito de imagem de 1 1 ao pré-testar previamente como o efeito mapeia entradas para saídas para um subconjunto de todos os valores de entrada.
ms.assetid: 2f0b4b6d-f371-101c-918a-bf564778e593
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b6d7cee4d21af5f7bc56ee4982f64523e892e616263b3cf5ed7ea84294fbb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161017"
---
# <a name="3d-lookup-table-effect"></a>efeito de tabela de pesquisa 3D

Uma tabela de pesquisa 3D é um efeito de uso geral que é usado para encapsular qualquer efeito de imagem de 1:1 ao pré-testar previamente como o efeito mapeia entradas para saídas para um subconjunto de todos os valores de entrada.

O efeito da tabela de pesquisa 3D (LUT) modifica uma imagem de entrada usando o valor de cor RGB da imagem para indexar uma textura 3D, em que a textura contém um valor de saída preputado de um pipeline de efeito arbitrário.

O LUT 3D deve ser carregado em um recurso de textura de GPU para ser renderizado, e isso pode ser caro dependendo do tamanho da textura e dos recursos do dispositivo. Os desenvolvedores de aplicativos podem especificar quando pagar esse custo usando o recurso [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D. **ID2D1LookupTable3D** tem os seguintes atributos:

-   Fornece uma representação abstrata do recurso de GPU do 3D LUT.
-   Dependendo dos recursos do dispositivo, uma textura 2D ou 3D será criada e preenchida com os dados LUT fornecidos.
-   Pode ser passado para a propriedade do efeito LUT 3D para renderização.

O CLSID para esse efeito é CLSID \_ D2D1LookupTable3D.

-   [Imagem de exemplo](#example-image)
-   [Código de exemplo](#sample-code)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/3dlookuptable-effect.png)

## <a name="sample-code"></a>Código de exemplo

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

## <a name="effect-properties"></a>Propriedades do efeito

As propriedades do efeito da tabela de pesquisa 3D são definidas pela enumeração de [**\_ \_ prop d2d1 LOOKUPTABLE3D**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
