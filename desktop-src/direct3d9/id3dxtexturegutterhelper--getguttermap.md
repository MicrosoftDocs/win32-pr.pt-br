---
description: Recebe um valor de classe texel que indica a classe texel de acordo com o local de cada texel.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: Método ID3DXTextureGutterHelper::GetGutterMap (D3DX9Mesh.h)
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
ms.openlocfilehash: 8ef2ed7b088e54dd82b1cc99422e1488139199ffe034e810de8e0a0bdb242f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095686"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>Método ID3DXTextureGutterHelper::GetGutterMap

Recebe um valor de classe texel que indica a classe texel de acordo com o local de cada texel.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGutterData* \[ in, out\]
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)\***

Ponteiro para a classe texel. As possíveis classes de texel são as a seguir. Não há nenhuma classe de texel 3.



| Classe Texel | Localização do Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Ponto inválido; não será usado.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Dentro do triângulo.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Dentro da medianiz.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Dentro da medianiz; O texel será avaliado como um exemplo completo nos métodos [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper::ApplyGuttersPRT.**](id3dxtexturegutterhelper--applyguttersprt.md) |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

O aplicativo deve alocar e gerenciar pGutterData, com o tamanho determinado por:


```
texture width * texture height * sizeof(BYTE)
```



A largura e a altura da textura são retornadas [**por ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) e [**ID3DXTextureGutterHelper::GetHeight.**](id3dxtexturegutterhelper--getheight.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
