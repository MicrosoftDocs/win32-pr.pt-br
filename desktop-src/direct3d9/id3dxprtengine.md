---
description: A interface ID3DXPRTEngine é usada para calcular uma simulação de transferência de radiante (PRT) de computação. Seus métodos normalmente são usados offline, para computar vetores de transferência por vértice ou por Texel antes da modelagem 3D em tempo real.
ms.assetid: d5be657f-2b0c-48fd-a7f0-ddb90107772f
title: Interface ID3DXPRTEngine (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5507a79a60b2ffcb3cf801ea0454c7306bcde056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780350"
---
# <a name="id3dxprtengine-interface"></a>Interface ID3DXPRTEngine

A interface ID3DXPRTEngine é usada para calcular uma simulação de transferência de radiante (PRT) de computação. Seus métodos normalmente são usados offline, para computar vetores de transferência por vértice ou por Texel antes da modelagem 3D em tempo real.

## <a name="members"></a>Membros

A interface **ID3DXPRTEngine** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTEngine** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXPRTEngine** tem esses métodos.



| Método                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)                       | Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha. Se uma interseção for encontrada, o método retornará o índice da face de malha mais próxima atingida pelas coordenadas Ray e barycentric do ponto de interseção.<br/>                                                                                                                                                                                |
| [**ComputeBounce**](id3dxprtengine--computebounce.md)                                     | Computa a radiante de origem resultante de um único salto de luz interrefletida. Esse método pode ser usado para qualquer cena acesa, incluindo um modelo de PRT (computação radiante) com base em harmônica esférica (SH).<br/>                                                                                                                                                                                                                                                    |
| [**ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)                     | Computa a radiante de origem resultante de um único salto de luz interrefletida, usando a amostragem adaptável. Esse método gera novos vértices e rostos na malha para aproximar com mais precisão o sinal de radiante de transferência (PRT) de computação. Esse método pode ser usado para qualquer cena acesa, incluindo um modelo de PRT baseado em harmônica esférica (SH).<br/>                                                                                                                   |
| [**ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)                 | Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH).<br/>                                                                                                                                                                                                                                                                                                                            |
| [**ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) | Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH), usando a amostragem adaptável. Esse método gera novos vértices e rostos na malha para aproximar com mais precisão o sinal de radiante de transferência (PRT) de computação.<br/>                                                                                                                                                           |
| [**ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md)           | Usa a GPU para calcular a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica (SH) esférica. A computação da iluminação na GPU geralmente será muito mais rápida do que na CPU.<br/>                                                                                                                                                                                                                            |
| [**ComputeLDPRTCoeffs**](id3dxprtengine--computeldprtcoeffs.md)                           | Computa coeficientes de LDPRT (transferência de radiante precomputada) de forma local em relação aos vetores normais por amostra para minimizar o erro de quadrados mínimos em relação aos dados de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada. Esses coeficientes podem ser usados com vetores normais de aparência ou transformação para modelar efeitos globais em objetos dinâmicos.<br/>                                                                                                                     |
| [**Computação**](id3dxprtengine--computess.md)                                             | Computa o radiante de origem resultante da dispersão de subsuperfície, usando as propriedades de material definidas por [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). Esse método pode ser usado somente para materiais definidos por vértice em um objeto de malha.<br/>                                                                                                                                                                                                       |
| [**ComputeSSAdaptive**](id3dxprtengine--computessadaptive.md)                             | Computa um vetor de transferência que mapeia o radiante de origem para sair do radiante resultante da dispersão de subsuperfície, usando a amostragem adaptável e as propriedades de material definidas por [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). O método gera novos vértices e rostos na malha para aproximar com mais precisão o sinal de radiante de transferência (PRT) precomputado. Esse método pode ser usado somente para materiais definidos por vértice em um objeto de malha.<br/> |
| [**ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)               | Computa amostras de PRT (transferência de radiante de computação) para um ponto arbitrário (e um vetor normal).<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)           | Computa, em um ponto arbitrário que não está em uma malha, um vetor de transferência que mapeia radiante de origem (representado por uma aproximação harmônica esférica (SH)) para sair de radiante.<br/>                                                                                                                                                                                                                                                                                                   |
| [**ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)                       | Computa uma projeção da iluminação direta da luz anterior devolvida em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.<br/>                                                                                                                                                                                                                                                                                         |
| [**ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)       | Computa uma projeção de iluminação distante em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ExtractPerVertexAlbedo**](id3dxprtengine--extractpervertexalbedo.md)                   | Copia valores de albedo por vértice de uma malha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**FreeBounceData**](id3dxprtengine--freebouncedata.md)                                   | Libera a memória usada para dados temporários de simulação de luz devolvida.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**FreeSSData**](id3dxprtengine--freessdata.md)                                           | Libera a memória usada para dados de simulação de dispersão de luz temporárias de subsuperfície.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**GetAdaptedMesh**](id3dxprtengine--getadaptedmesh.md)                                   | Retorna uma malha com modificações resultantes da amostragem espacial adaptável. A malha retornada contém apenas posições, normais e coordenadas de textura (se definido).<br/>                                                                                                                                                                                                                                                                                                   |
| [**GetNumFaces**](id3dxprtengine--getnumfaces.md)                                         | Recupera o número de faces na malha, incluindo quaisquer faces novas adicionadas como resultado da amostragem espacial adaptável.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetNumVerts**](id3dxprtengine--getnumverts.md)                                         | Recupera o número de vértices na malha, incluindo quaisquer novos vértices adicionados como resultado da amostragem espacial adaptável.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetVertexAlbedo**](id3dxprtengine--getvertexalbedo.md)                                 | Recupera os valores de albedo dos vértices de malha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md)                                   | Multiplica cada vetor de PRT (transferência radiante em pré-computação) pelo albedo por vértice.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ResampleBuffer**](id3dxprtengine--resamplebuffer.md)                                   | Reamostrar um buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada e salvá-lo em um buffer de saída. Esse método pode ser usado para converter um buffer de vértice em um buffer de textura e vice-versa. Ele também pode ser usado para converter buffers de canal único em buffers de 3 canais e vice-versa.<br/>                                                                                                                                                                                  |
| [**RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)                               | Subdivide faces em uma malha, permitindo uma amostragem adaptável conservadora que não eliminará os recursos na malha.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**ScaleMeshChunk**](id3dxprtengine--scalemeshchunk.md)                                   | Dimensiona todos os exemplos associados a uma determinada submalha. O método é útil para computar a dispersão da subsuperfície.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetCallback**](id3dxprtengine--setcallback.md)                                         | Define um ponteiro para uma função de retorno de chamada opcional que calcula a porcentagem de cálculos de harmônica esférica (SH) concluídas e dá ao chamador a opção de anular o simulador.<br/>                                                                                                                                                                                                                                                                               |
| [**SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)                               | Define as propriedades de material de malha na cena 3D. Use este método para especificar os parâmetros de dispersão de subsuperfície.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)                     | Define as distâncias mínimas e máximas de interseção entre objetos 3D. Esses valores de distância podem ser usados para controlar a distância mínima ou máxima que os objetos podem sombrear ou refletir a luz. Por exemplo, o método pode ser usado para limitar a sombra dos recursos próximos de um modelo 3D.<br/>                                                                                                                                                                          |
| [**SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md)                             | Define um valor de albedo para cada Texel, substituindo valores albedo anteriores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**SetPerTexelNormal**](id3dxprtengine--setpertexelnormal.md)                             | Define um vetor normal para cada Texel em um objeto de textura. Esse método é usado para armazenar vetores normais de vértice de uma malha (ou um vértice interpolado Normals se a transferência de radiante (PRT) baseada em pixels estiver sendo computada).<br/>                                                                                                                                                                                                                                          |
| [**SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)                           | Define um valor de albedo para cada vértice de malha, substituindo valores de albedo anteriores.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)                                 | Define as propriedades de amostragem usadas pelo simulador de transferência de radiante (PRT) precomputado.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)                         | Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha. Normalmente usado para determinar se um determinado ponto está em sombra.<br/>                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

Para converter de RGB em valores de luminância, a fórmula a seguir é usada:


```
Luminance = R * 0.2125 + G * 0.7154 + B * 0.0721
```



A interface **ID3DXPRTEngine** é obtida chamando a função [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) .

O tipo LPD3DXPRTENGINE é definido como um ponteiro para a interface **ID3DXPRTEngine** .


```
typedef interface ID3DXPRTEngine ID3DXPRTEngine;
typedef interface ID3DXPRTEngine *LPD3DXPRTENGINE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)
</dt> <dt>

[Transferência radiante de computação (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
