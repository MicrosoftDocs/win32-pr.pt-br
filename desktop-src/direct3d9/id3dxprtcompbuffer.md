---
description: A interface ID3DXPRTCompBuffer armazena uma versão compactada de um buffer ID3DXPRTBuffer para uso com o PCA (análise de componente principal).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Interface ID3DXPRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a84f1bc7b25af0c900f5587ba0d1dd948cac39bc52f706ff389c0ca9d053ec0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985606"
---
# <a name="id3dxprtcompbuffer-interface"></a>Interface ID3DXPRTCompBuffer

A interface **ID3DXPRTCompBuffer** armazena uma versão compactada de um buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) para uso com o PCA (análise de componente principal).

## <a name="members"></a>Membros

A interface **ID3DXPRTCompBuffer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTCompBuffer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXPRTCompBuffer** tem esses métodos.



| Método                                                             | Descrição                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtractBasis**](id3dxprtcompbuffer--extractbasis.md)           | Extrai os vetores de base de ACP (análise de componente principal) para um determinado cluster de um buffer de dados compactado **ID3DXPRTCompBuffer** .<br/>                                                                       |
| [**ExtractClusterIDs**](id3dxprtcompbuffer--extractclusterids.md) | Extrai as IDs de cluster por amostra de um buffer de dados compactado **ID3DXPRTCompBuffer** .<br/>                                                                                                                              |
| [**ExtractPCA**](id3dxprtcompbuffer--extractpca.md)               | Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado **ID3DXPRTCompBuffer** .<br/>                                                                               |
| [**ExtractTexture**](id3dxprtcompbuffer--extracttexture.md)       | Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado **ID3DXPRTCompBuffer** e adiciona os dados a um objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/> |
| [**ExtractToMesh**](id3dxprtcompbuffer--extracttomesh.md)         | Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado **ID3DXPRTCompBuffer** e adiciona os dados a um objeto [**ID3DXMesh**](id3dxmesh.md) .<br/>                 |
| [**GetHeight**](id3dxprtcompbuffer--getheight.md)                 | Recupera a altura da textura, em pixels.<br/>                                                                                                                                                                         |
| [**GetNumChannels**](id3dxprtcompbuffer--getnumchannels.md)       | Recupera o número de canais de cores usados na memória para armazenar amostras.<br/>                                                                                                                                                 |
| [**GetNumClusters**](id3dxprtcompbuffer--getnumclusters.md)       | Recupera o número de clusters a serem usados para compactação.<br/>                                                                                                                                                                |
| [**GetNumCoeffs**](id3dxprtcompbuffer--getnumcoeffs.md)           | Recupera o número de escalares por canal de cor usado na memória para armazenar amostras.<br/>                                                                                                                                      |
| [**GetNumPCA**](id3dxprtcompbuffer--getnumpca.md)                 | Recupera o número de vetores de base do PCA (análise de componente principal) a serem usados em cada cluster.<br/>                                                                                                                        |
| [**GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md)         | Recupera o número de vértices (ou texels) amostrados.<br/>                                                                                                                                                                   |
| [**GetWidth**](id3dxprtcompbuffer--getwidth.md)                   | Recupera a largura da textura, em pixels.<br/>                                                                                                                                                                          |
| [**Istexture**](id3dxprtcompbuffer--istexture.md)                 | Indica se o buffer contém uma textura.<br/>                                                                                                                                                                        |
| [**NormalizeData**](id3dxprtcompbuffer--normalizedata.md)         | Normaliza todos os pesos do PCA (análise de componente principal) para que fiquem entre-1 e 1. Os vetores de base são modificados para refletir essa normalização.<br/>                                                                  |



 

## <a name="remarks"></a>Comentários

A interface **ID3DXPRTCompBuffer** é obtida chamando a função [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) .

O tipo LPD3DXPRTCOMPBUFFER é definido como um ponteiro para a interface **ID3DXPRTCompBuffer** .


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
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

[**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> </dl>

 

 
