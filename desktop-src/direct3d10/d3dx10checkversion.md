---
description: Função D3DX10CheckVersion – Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Função D3DX10CheckVersion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fc8befa88fb706965a30224843745b033ea205b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105344"
---
# <a name="d3dx10checkversion-function"></a>Função D3DX10CheckVersion

Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*D3DSdkVersion* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Use a \_ versão do SDK do d3d10 \_ . Consulte Observações.

</dd> <dt>

*D3DX10SdkVersion* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Use a \_ versão do SDK do D3DX10 \_ . Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a versão não corresponder, a função retornará FALSE (um número menor ou igual a 0, o número em si não terá significado).

## <a name="remarks"></a>Comentários

Use essa função durante a inicialização do seu aplicativo.


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
