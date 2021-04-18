---
description: Recebe um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'Método ID3DXTextureGutterHelper:: GetGutterMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105751365"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>Método ID3DXTextureGutterHelper:: GetGutterMap

Recebe um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGutterData* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)\***

Ponteiro para a classe Texel. As classes Texel possíveis são as seguintes. Não há nenhuma classe de Texel 3.



| Classe Texel | Local Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Ponto inválido; Texel não será usado.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Triângulo interno.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Dentro da medianiz.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Na medianiz; Texel será avaliado como um exemplo completo nos métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

O aplicativo deve alocar e gerenciar pGutterData, com o tamanho fornecido por:


```
texture width * texture height * sizeof(BYTE)
```



A largura e a altura da textura são retornadas por [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md) e [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
