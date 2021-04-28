---
description: Função D3DXCheckVersion – Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Função D3DXCheckVersion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 077d64a67a46080a0f7ac9194c684f6fe8470453
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115974"
---
# <a name="d3dxcheckversion-function"></a>Função D3DXCheckVersion

Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.

## <a name="syntax"></a>Sintaxe


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*D3DSDKVersion* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Use a \_ versão do SDK do D3D \_ . Consulte Observações.

</dd> <dt>

*D3DXSDKVersion* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Use a \_ versão do SDK do D3DX \_ . Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Retornará **true** se a versão do D3DX que você compilou for a versão com a qual você está executando; caso contrário, **false** será retornado.

## <a name="remarks"></a>Comentários

Use essa função durante a inicialização do seu aplicativo da seguinte maneira:


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) para verificar se o tempo de execução correto está instalado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de Uso Geral](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
