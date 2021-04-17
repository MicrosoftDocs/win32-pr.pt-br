---
description: Filtra os níveis de mipmap de uma textura.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Função D3DXFilterTexture (D3dx9tex. h)
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
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785270"
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

*pBaseTexture* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Ponteiro para uma interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que representa o objeto de textura a ser filtrado.

</dd> <dt>

*pPalette* \[ fora\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa uma paleta de cor de 256 para preencher ou **nulo** para formatos nonpalettized. Se uma paleta não for especificada, a paleta padrão do Direct3D (uma paleta branca opaca) será fornecida. Consulte Observações.

</dd> <dt>

*SrcLevel* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Nível cuja imagem é usada para gerar os níveis subsequentes. A especificação \_ do padrão D3DX para esse parâmetro é equivalente à especificação de 0.

</dd> <dt>

*MipFilter* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como o mipmap é filtrado. A especificação de D3DX \_ padrão para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ se o tamanho da textura for uma potência de dois e D3DX \_ caixa de filtro D3DX de filtro de \_ \| \_ \_ outra forma.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Um filtro é aplicado recursivamente a cada nível de textura para gerar o próximo nível de textura.

Gravar em uma superfície de não nível zero da textura não fará com que o retângulo sujo seja atualizado. Se **D3DXFilterTexture** for chamado e a superfície já não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explicitamente na textura.

As texturas criadas no pool padrão (D3DPOOL \_ padrão) não podem ser usadas com **D3DXFilterTexture** (a menos que criadas com D3DUSAGE \_ dinâmico), pois uma operação de bloqueio é necessária no objeto. Observe que os bloqueios são proibidos em texturas no pool padrão (a menos que sejam dinâmicos).

Para obter detalhes sobre o [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), consulte o SDK da plataforma. Observe que, a partir do DirectX 8,0, o membro peFlags da estrutura **PaletteEntry** não funciona conforme documentado no SDK da plataforma. O membro peFlags agora é o canal alfa para formatos de palettized de 8 bits.

Há apenas uma função de filtragem de textura, mas duas macros que chamam esse método.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
