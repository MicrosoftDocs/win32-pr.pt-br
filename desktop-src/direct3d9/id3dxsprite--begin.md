---
description: Prepara um dispositivo para desenhar sprites.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'Método ID3DXSprite:: Begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764166"
---
# <a name="id3dxspritebegin-method"></a>Método ID3DXSprite:: Begin

Prepara um dispositivo para desenhar sprites.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de zero ou mais sinalizadores que descrevem as opções de renderização de Sprite. Para esse método, os sinalizadores válidos são:

-   D3DXSPRITE \_ ALPHABLEND
-   D3DXSPRITE de \_ \_ mensagem
-   D3DXSPRITE \_ DONOTMODIFY \_ renderingstate
-   D3DXSPRITE \_ DONOTSAVESTATE
-   D3DXSPRITE \_ OBJECTspace
-   D3DXSPRITE \_ \_ \_ BACKTOFRONT profundidade de classificação \_
-   D3DXSPRITE \_ \_ \_ FRONTTOBACK profundidade de classificação \_
-   \_ \_ Textura de classificação D3DXSPRITE \_

Para obter uma descrição dos sinalizadores e informações sobre como controlar a captura de estado do dispositivo e as transformações de exibição do dispositivo, consulte [D3DXSPRITE](d3dxsprite.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método deve ser chamado de dentro de um [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) . . . Sequência [**IDirect3DDevice9:: endcena**](/windows/desktop/api) . **ID3DXSprite:: Begin** não pode ser usado como um substituto para **IDirect3DDevice9:: BeginScene** ou [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).

Esse método irá definir os seguintes Estados no dispositivo.

Processar estados:



| Tipo ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) | Valor                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3DRS \_ ALPHABLENDENABLE                                       | TRUE                                                                                                              |
| D3DRS \_ ALPHAFUNC                                              | D3DCMP \_ maior                                                                                                   |
| D3DRS \_ ALPHAREF                                               | 0x00                                                                                                              |
| D3DRS \_ ALPHATESTENABLE                                        | AlphaCmpCaps                                                                                                      |
| D3DRS \_ BLENDOP                                                | D3DBLENDOP \_ Adicionar                                                                                                   |
| Recorte de D3DRS \_                                               | TRUE                                                                                                              |
| D3DRS \_ CLIPPLANEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ COLORWRITEENABLE                                       | D3DCOLORWRITEENABLE \_ Alpha \| D3DCOLORWRITEENABLE \_ Blue \| D3DCOLORWRITEENABLE \_ verde \| D3DCOLORWRITEENABLE \_ vermelho |
| D3DRS de \_ seleção                                               | D3DCULL \_ nenhum                                                                                                     |
| D3DRS \_ DESTBLEND                                              | D3DBLEND \_ INVSRCALPHA                                                                                             |
| D3DRS \_ DiffuseMaterialSource                                  | D3DMCS \_ COLOR1                                                                                                    |
| D3DRS \_ ENABLEADAPTIVETESSELLATION                             | FALSE                                                                                                             |
| D3DRS \_ FillMode                                               | D3DFILL \_ sólido                                                                                                    |
| D3DRS \_ FOGENABLE                                              | FALSE                                                                                                             |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE                               | FALSE                                                                                                             |
| \_Iluminação D3DRS                                               | FALSE                                                                                                             |
| D3DRS \_ RANGEFOGENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SEPARATEALPHABLENDENABLE                               | FALSE                                                                                                             |
| D3DRS \_ shadmode                                              | D3DSHADE \_ GOURAUD                                                                                                 |
| D3DRS \_ SPECULARENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SRCBLEND                                               | D3DBLEND \_ SRCALPHA                                                                                                |
| D3DRS \_ SRGBWRITEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ STENCILENABLE                                          | FALSE                                                                                                             |
| D3DRS \_ VERTEXBLEND                                            | FALSE                                                                                                             |
| D3DRS \_ WRAP0                                                  | 0                                                                                                                 |



 

Estados de estágio de textura:



| Identificador de estágio | Tipo ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) | Valor            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | D3DTSS \_ ALPHAARG1                                                         | \_Textura D3DTA   |
| 0                | D3DTSS \_ ALPHAARG2                                                         | D3DTA \_ difuso   |
| 0                | D3DTSS \_ ALPHAOP                                                           | \_Modular D3DTOP |
| 0                | D3DTSS \_ COLORARG1                                                         | \_Textura D3DTA   |
| 0                | D3DTSS \_ COLORARG2                                                         | D3DTA \_ difuso   |
| 0                | D3DTSS \_ COLOROP                                                           | \_Modular D3DTOP |
| 0                | D3DTSS \_ TEXCOORDINDEX                                                     | 0                |
| 0                | D3DTSS \_ TEXTURETRANSFORMFLAGS                                             | D3DTTFF \_ desabilitar |
| 1                | D3DTSS \_ ALPHAOP                                                           | D3DTOP \_ desabilitar  |
| 1                | D3DTSS \_ COLOROP                                                           | D3DTOP \_ desabilitar  |



 

Estados de amostra:



| Índice de estágio de amostra | Tipo ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) | Valor                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | Endereço de D3DSAMP \_                                               | D3DTADDRESS \_ fixe                                                                                             |
| 0                   | D3DSAMP \_ ADDRESSV                                               | D3DTADDRESS \_ fixe                                                                                             |
| 0                   | D3DSAMP \_ MAGFILTER                                              | D3DTEXF \_ ANISOTROPIC se TextureFilterCaps incluir D3DPTFILTERCAPS \_ MAGFANISOTROPIC; caso contrário, D3DTEXF \_ linear |
| 0                   | D3DSAMP \_ MAXMIPLEVEL                                            | 0                                                                                                              |
| 0                   | D3DSAMP \_ MAXANISOTROPY                                          | MaxAnisotropy                                                                                                  |
| 0                   | D3DSAMP \_ MINFILTER                                              | D3DTEXF \_ ANISOTROPIC se TextureFilterCaps incluir D3DPTFILTERCAPS \_ MINFANISOTROPIC; caso contrário, D3DTEXF \_ linear |
| 0                   | D3DSAMP \_ MIPFILTER                                              | D3DTEXF \_ linear se TextureFilterCaps inclui D3DPTFILTERCAPS \_ MIPFLINEAR; caso contrário, D3DTEXF \_ ponto            |
| 0                   | D3DSAMP \_ MIPMAPLODBIAS                                          | 0                                                                                                              |
| 0                   | D3DSAMP \_ SRGBTEXTURE                                            | 0                                                                                                              |



 

> [!Note]  
> Esse método desabilita N-patches.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 
