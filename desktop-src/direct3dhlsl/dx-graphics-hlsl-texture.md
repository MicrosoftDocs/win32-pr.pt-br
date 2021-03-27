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
# <a name="texture-type"></a>Tipo de textura

Use a sintaxe a seguir para declarar uma variável de textura.

|                |
|----------------|
| **Nome do tipo;** |

## <a name="parameters"></a>Parâmetros
| Item                                                                                     | Descrição                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Escreva**<br/> | Um dos seguintes tipos: Texture (não tipado, para compatibilidade com versões anteriores), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube. O tamanho do elemento deve caber em quantidades de 4 32 bits.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/> | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                                                                                                                                                   |
## <a name="remarks"></a>Comentários

Há três partes para usar uma textura.

1.  Declarando uma variável de textura. Isso é feito com a sintaxe mostrada acima. Por exemplo, são declarações válidas.

    ```
    texture g_MeshTexture;
    ```

    \- ou –

    ```
    Texture2D g_MeshTexture;
    ```

2.  Declarando e inicializando um objeto de amostra. Isso é feito com uma sintaxe ligeiramente diferente no Direct3D 9 e no Direct3D 10. Para obter detalhes sobre a sintaxe do objeto de amostra, consulte [tipo de amostra (DirectX HLSL)](dx-graphics-hlsl-sampler.md).
3.  Invocar uma função de textura em um sombreador.

Diferenças entre o Direct3D 9 e o Direct3D 10:

O Direct3D 9 usa [funções de textura intrínsecas](dx-graphics-hlsl-intrinsic-functions.md) para executar operações de textura. Este exemplo é do [exemplo BasicHLSL](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) e usa [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) para executar a amostragem de textura.

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

O Direct3D 10 usa [objetos de textura de modelo](dx-graphics-hlsl-to-type.md) em vez disso. Aqui está um exemplo da operação de textura equivalente.

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a>Confira também

[Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
