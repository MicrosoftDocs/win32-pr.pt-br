---
description: Define as propriedades de amostragem usadas pelo simulador de transferência de radiante (PRT) precomputado.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'Método ID3DXPRTEngine:: SetSamplingInfo (D3DX9Mesh. h)'
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
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664031"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>Método ID3DXPRTEngine:: SetSamplingInfo

Define as propriedades de amostragem usadas pelo simulador de transferência de radiante (PRT) precomputado.

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

*NumRays* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de raios claros para direcionar a cada amostra. Deve ser maior que zero.

</dd> <dt>

*UseSphere* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **for true**, os exemplos serão computados em uma esfera completa. Se **for falso**, os exemplos serão computados em um hemisfério.

</dd> <dt>

*UseCosine* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **for true**, use um peso cosseno de exemplos. Se UseCosine e UseSphere forem **true**, o método falhará e um erro será retornado.

</dd> <dt>

*Adaptável* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Deve ser **false**. A amostragem adaptável não está implementada no momento.

</dd> <dt>

*AdaptiveThresh* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, e \_ NOTIMPL, e \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
