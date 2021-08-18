---
description: A interface ID3DXPRTBuffer é usada como um buffer de dados para armazenar dados de vértice e pixel para uso com funções e métodos de PRT (transferência de radiance pré-comutada).
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Interface ID3DXPRTBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69f4a40055adea1440436cc54cecc5735db95bc01787cb779cc8a7d6c51b0011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120540"
---
# <a name="id3dxprtbuffer-interface"></a>Interface ID3DXPRTBuffer

A interface ID3DXPRTBuffer é usada como um buffer de dados para armazenar dados de vértice e pixel para uso com funções e métodos de PRT (transferência de radiance pré-comutada).

## <a name="members"></a>Membros

A interface **ID3DXPRTBuffer** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPRTBuffer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXPRTBuffer** tem esses métodos.



| Método                                                   | Descrição                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBuffer**](id3dxprtbuffer--addbuffer.md)           | Adiciona outro buffer ao **ID3DXPRTBuffer** e armazena os resultados **em ID3DXPRTBuffer**.<br/>                                                                                        |
| [**AttachGH**](id3dxprtbuffer--attachgh.md)             | Associa um [**objeto ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) ao **objeto ID3DXPRTBuffer.**<br/>                                                              |
| [**EvalGH**](id3dxprtbuffer--evalgh.md)                 | Aplica dados armazenados de medianiz de textura a um buffer de textura **ID3DXPRTBuffer.**<br/>                                                                                                        |
| [**ExtractTexture**](id3dxprtbuffer--extracttexture.md) | Extrai dados de coeficiente de um canal de cores do buffer para um intervalo especificado de coeficientes e adiciona os dados a [**um objeto IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)<br/> |
| [**ExtractToMesh**](id3dxprtbuffer--extracttomesh.md)   | Extrai dados de coeficiente de um buffer de canal único e adiciona os dados a um [**objeto ID3DXMesh.**](id3dxmesh.md)<br/>                                                              |
| [**Getheight**](id3dxprtbuffer--getheight.md)           | Recupera a altura da textura, em pixels.<br/>                                                                                                                                    |
| [**GetNumChannels**](id3dxprtbuffer--getnumchannels.md) | Recupera o número de canais de cores usados na memória para armazenar amostras.<br/>                                                                                                            |
| [**GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)     | Recupera o número de escalares por canal de cores usado na memória para armazenar amostras.<br/>                                                                                                 |
| [**GetNumSamples**](id3dxprtbuffer--getnumsamples.md)   | Recupera o número de vértices (ou texels) amostrados.<br/>                                                                                                                              |
| [**Getwidth**](id3dxprtbuffer--getwidth.md)             | Recupera a largura da textura, em pixels.<br/>                                                                                                                                     |
| [**IsTexture**](id3dxprtbuffer--istexture.md)           | Indica se o buffer contém uma textura.<br/>                                                                                                                                   |
| [**Lockbuffer**](id3dxprtbuffer--lockbuffer.md)         | Bloqueia um intervalo de dados de exemplo de vértice ou texel e obtém um ponteiro para o local na memória do buffer.<br/>                                                                               |
| [**ReleaseGH**](id3dxprtbuffer--releasegh.md)           | Desassocia um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) anexado ao **objeto ID3DXPRTBuffer.**<br/>                                                   |
| [**Redimensionar**](id3dxprtbuffer--resize.md)                 | Altera o número de amostras contidas no buffer.<br/>                                                                                                                             |
| [**ScaleBuffer**](id3dxprtbuffer--scalebuffer.md)       | Multiplica cada valor no buffer por um valor constante.<br/>                                                                                                                          |
| [**Unlockbuffer**](id3dxprtbuffer--unlockbuffer.md)     | Encerra o tempo de vida do ponteiro ppData retornado [**por ID3DXPRTBuffer::LockBuffer.**](id3dxprtbuffer--lockbuffer.md)<br/>                                                              |



 

## <a name="remarks"></a>Comentários

A interface **ID3DXPRTBuffer** é obtida chamando as funções [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) ou [**D3DXCreatePRTBufferTex.**](d3dxcreateprtbuffertex.md)

O tipo LPD3DXPRTBUFFER é definido como um ponteiro para a interface **ID3DXPRTBuffer.**


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
