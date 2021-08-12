---
description: Define as propriedades de amostragem usadas pelo simulador de PRT (transferência de radiance pré-comutada).
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: Método ID3DXPRTEngine::SetSamplingInfo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db15bc2120f90cf52aa4f3c41eccecc7d308cc8392ae368cd4423a90f218f6ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293360"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>Método ID3DXPRTEngine::SetSamplingInfo

Define as propriedades de amostragem usadas pelo simulador de PRT (transferência de radiance pré-comutada).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumRays* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de raios de luz a direcionar em cada amostra. Deve ser maior que zero.

</dd> <dt>

*UseSphere* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE**, os exemplos serão computados em uma esfera inteira. Se **FALSE**, as amostras serão computadas em um continente.

</dd> <dt>

*UseCosine* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE**, use uma ponderação cosseno de amostras. Se UseCosine e UseSphere são **TRUE,** o método falhará e um erro será retornado.

</dd> <dt>

*Adaptável* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Deve ser **FALSE.** No momento, a amostragem adaptável não está implementada.

</dd> <dt>

*AdaptiveThresh* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ NOTIMPL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
