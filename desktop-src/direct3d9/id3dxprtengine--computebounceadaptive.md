---
description: Calcula o radiamento de origem resultante de um único salto de luz interreflecionado, usando a amostragem adaptável.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: Método ID3DXPRTEngine::ComputeBounceAdaptive (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: efe983a0160d46910e7b8d1e29d0042d801275ef70aef30f6050e0538b6f9927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729745"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a>Método ID3DXPRTEngine::ComputeBounceAdaptive

Calcula o radiamento de origem resultante de um único salto de luz interreflecionado, usando a amostragem adaptável. Esse método gera novos vértices e faces na malha para aproximar com mais precisão o sinal de PRT (transferência de radiance pré-comutada). Esse método pode ser usado para qualquer cena com iluminação, incluindo um modelo PRT baseado em SH (metal esférico).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDataIn* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) entrada que representa o objeto 3D do salto de luz anterior. Esse buffer de entrada deve ter o número adequado de canais de cores alocados para a simulação.

</dd> <dt>

*AdaptiveThresh* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Limite no vetor PRT a ser usado para subdividir vértices e faces de malha. Se for menor que 1e-6f, um valor padrão de 1e-6f será especificado.

</dd> <dt>

*MinEdgeLength* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Comprimento mínimo da borda facial que será gerado na amostragem adaptável. Se o método determinar que o valor é muito pequeno, um valor dependente do modelo será especificado. Se zero, um valor padrão de 4 será especificado.

</dd> <dt>

*MaxSubdiv* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nível máximo de subdivisão de um rosto que será usado na amostragem adaptável.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) saída. Esse buffer de saída deve ter o número adequado de canais de cores alocados para a simulação.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que mantém uma soma em execução de pDataOut com cada computação de salto leve. Pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
