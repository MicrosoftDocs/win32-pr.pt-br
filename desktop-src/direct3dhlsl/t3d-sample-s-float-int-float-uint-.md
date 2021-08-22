---
title: Função Texture3D::Sample(S,float,int,float,uint)
description: Amostra uma textura com um valor opcional para fixar valores de LOD (nível de detalhes) de exemplo e retorna o status da operação. | Função Texture3D::Sample(S,float,int,float,uint)
ms.assetid: DB8401A1-1065-4616-BDDE-9ADB59B09C8B
keywords:
- Função de exemplo HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ee3df71ebe12be050cf7f9b2c2160c36ed408a4250f17083bf493daa8b35e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788178"
---
# <a name="texture3dsamplesfloatintfloatuint-function"></a>Função Texture3D::Sample(S,float,int,float,uint)

Amostra uma textura com um valor opcional para fixar valores de LOD (nível de detalhes) de exemplo e retorna o status da operação.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*S* \[ em\]
</dt> <dd>

Um [estado sampler](dx-graphics-hlsl-sampler.md). Esse é um objeto declarado em um arquivo de efeito que contém atribuições de estado.

</dd> <dt>

*Localização* \[ Em\]
</dt> <dd>

As coordenadas de textura. O tipo de argumento depende do tipo de objeto de textura.



| Texture-Object tipo                    | Tipo de parâmetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Deslocamento* \[ Em\]
</dt> <dd>

Um deslocamento de coordenada de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. Use um deslocamento somente em um miplevel inteiro; caso contrário, você poderá obter resultados que não são bem traduzidos para hardware. O tipo de argumento depende do tipo de objeto de textura. Para obter mais informações, consulte [Aplicando deslocamentos inteiros.](dx-graphics-hlsl-to-sample.md)



| Texture-Object tipo           | Tipo de parâmetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | sem suporte  |



 

</dd> <dt>

*Fixação* \[ Em\]
</dt> <dd>

Um valor opcional para fixar valores LOD de exemplo. Por exemplo, se você passar 2,0f para o valor de fixação, garantirá que nenhuma amostra individual acesse um nível de mip menor que 2,0f.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

O status da operação. Você não pode acessar o status diretamente; Em vez disso, passe o status para a [**função intrínseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** retornará **TRUE** se todos os valores  da operação de **Exemplo,** **Coletar** ou Carregar correspondente acessarem blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Se algum valor tiver sido retirado de um tile não mapeado, **CheckAccessFullyMapped** retornará **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O formato de textura, que é um dos valores digitados listados em [**FORMATO DXGI. \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de exemplo](texture3d-sample.md)
</dt> <dt>

[**Texture3D**](sm5-object-texture3d.md)
</dt> </dl>

 

 
