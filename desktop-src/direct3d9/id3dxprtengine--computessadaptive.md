---
description: Calcula um vetor de transferência que mapeia a radiação de origem para sair do radiance resultante da dispersão de subsuficiência, usando a amostragem adaptável e as propriedades de material definidas por ID3DXPRTEngine::SetMeshMaterials.
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: Método ID3DXPRTEngine::ComputeSSAdaptive (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a602566c4d0e5b3cb5c68b2f983b6c56a9d9f596ee673db97a72e6054837759b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847376"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>Método ID3DXPRTEngine::ComputeSSAdaptive

Calcula um vetor de transferência que mapeia a radiação de origem para sair do radiance resultante da dispersão de subsuperfigura, usando a amostragem adaptável e as propriedades de material definidas por [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). O método gera novos vértices e faces na malha para aproximar com mais precisão o sinal de PRT (transferência de radiance pré-comutada). Esse método pode ser usado somente para materiais definidos por vértice em um objeto de malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeSSAdaptive(
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

Comprimento mínimo da borda facial que será gerado na amostragem adaptável. Se o método determinar que o valor é muito pequeno, um valor dependente do modelo será especificado.

</dd> <dt>

*MaxSubdiv* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nível máximo de subdivisão de um rosto que será usado na amostragem adaptável. Se zero, um valor padrão de 4 será especificado.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um [**objeto ID3DXPRTBuffer de**](id3dxprtbuffer.md) saída que modela um único salto da luz dispersa de subsuperfigura. Esse buffer de saída deve ter o número adequado de canais de cores alocados para a simulação.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que é a soma em execução de todas as saídas pDataOut anteriores. Pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Para modelar o dispersão de subsuficiência, chame esse método para cada ressalto de luz depois que um método [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) for chamado.

A saída desse método não inclui o albedo e apenas a luz de entrada é integrada ao simulador. Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que o radiance de origem, ingando assim resultados mais precisos da compactação.

Chame [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor PRT pelo albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounce**](id3dxprtengine--computebounce.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeSS**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
