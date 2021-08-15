---
description: Filtra os níveis de mipmap de uma textura.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Função D3DXFilterTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc07336edb5f7bb8672fbbec415b0a3b312335a3a3a4b0de32aec4fdde558363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988496"
---
# <a name="d3dxfiltertexture-function"></a>Função D3DXFilterTexture

Filtra os níveis de mipmap de uma textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBaseTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Ponteiro para uma interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que representa o objeto de textura a ser filtrado.

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para uma [**estrutura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa uma paleta de 256 cores a ser preenchida ou **NULL** para formatos não sem formatação. Se uma paleta não for especificada, a paleta padrão do Direct3D (uma paleta branca opaca) será fornecida. Consulte Observações.

</dd> <dt>

*SrcLevel* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nível cuja imagem é usada para gerar os níveis subsequentes. Especificar D3DX \_ DEFAULT para esse parâmetro é equivalente a especificar 0.

</dd> <dt>

*MipFilter* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais [FILTRO D3DX \_ ](d3dx-filter.md) controlando como o mipmap é filtrado. Especificar D3DX DEFAULT para esse parâmetro é o equivalente a especificar D3DX FILTER BOX se o tamanho da textura for uma potência de \_ \_ dois e \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER DITHER caso \_ contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Um filtro é aplicado recursivamente a cada nível de textura para gerar o próximo nível de textura.

A escrita em uma superfície de nível zero da textura não fará com que o retângulo sujo seja atualizado. Se **D3DXFilterTexture** for chamado e a superfície ainda não estiver suja (isso é improvável em cenários de uso normal), o aplicativo precisará chamar explicitamente [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) na textura.

Texturas criadas no pool padrão (D3DPOOL DEFAULT) não podem ser usadas com \_ **D3DXFilterTexture** (a menos que criadas com D3DUSAGE DYNAMIC) porque uma operação de bloqueio é necessária no objeto \_ . Observe que os bloqueios são proibidos em texturas no pool padrão (a menos que sejam dinâmicos).

Para obter detalhes [**sobre PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)consulte o SDK da plataforma. Observe que, a partir do DirectX 8.0, o membro peFlags da estrutura **PALETTEENTRY** não funciona conforme documentado no SDK da Plataforma. O membro peFlags agora é o canal alfa para formatos palettized de 8 bits.

Há apenas uma função de filtragem de textura, mas duas macros que chamam esse método.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
