---
description: 'Computa um vetor de transferência que mapeia o radiante de origem para sair do radiante resultante da dispersão de subsuperfície, usando a amostragem adaptável e as propriedades de material definidas por ID3DXPRTEngine:: SetMeshMaterials.'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'Método ID3DXPRTEngine:: ComputeSSAdaptive (D3DX9Mesh. h)'
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
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793654"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>Método ID3DXPRTEngine:: ComputeSSAdaptive

Computa um vetor de transferência que mapeia o radiante de origem para sair do radiante resultante da dispersão de subsuperfície, usando a amostragem adaptável e as propriedades de material definidas por [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). O método gera novos vértices e rostos na malha para aproximar com mais precisão o sinal de radiante de transferência (PRT) precomputado. Esse método pode ser usado somente para materiais definidos por vértice em um objeto de malha.

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

*pDataIn* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa o objeto 3D do salto claro anterior. Esse buffer de entrada deve ter o número correto de canais de cores alocados para a simulação.

</dd> <dt>

*AdaptiveThresh* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Limite no vetor de PRT a ser usado para subdividir vértices de malha e rostos. Se for menor que 1e-6F, um valor padrão de 1e-6F será especificado.

</dd> <dt>

*MinEdgeLength* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Comprimento mínimo de borda facial que será gerado na amostragem adaptável. Se o método determinar que o valor é muito pequeno, um valor dependente de modelo será especificado.

</dd> <dt>

*MaxSubdiv* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Nível máximo de subdivisão de uma face que será usada na amostragem adaptável. Se for zero, um valor padrão de 4 será especificado.

</dd> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que modela um único salto da luz dispersa de subsuperfície. Esse buffer de saída deve ter o número correto de canais de cores alocados para a simulação.

</dd> <dt>

*pDataTotal* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que é a soma em execução de todas as saídas de pDataOut anteriores. Pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Para modelar a dispersão de subsuperfície, chame esse método para cada salto leve depois que um método [**ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) for chamado.

A saída desse método não inclui albedo, e apenas a luz de entrada é integrada ao simulador. Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.

Chame [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor de PRT pelo albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounce**](id3dxprtengine--computebounce.md)
</dt> <dt>

[**ID3DXPRTEngine:: computar**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
