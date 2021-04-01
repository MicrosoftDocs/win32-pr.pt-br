---
description: Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH), usando a amostragem adaptável.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'Método ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664114"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>Método ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive

Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH), usando a amostragem adaptável. Esse método gera novos vértices e rostos na malha para aproximar com mais precisão o sinal de radiante de transferência (PRT) de computação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*AdaptiveThresh* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Limite no vetor de PRT a ser usado para subdividir vértices de malha e rostos. Se for menor que 1e-6F, um valor padrão de 1e-6F será especificado.

</dd> <dt>

*MinEdgeLength* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Comprimento mínimo de borda facial que será gerado na amostragem adaptável. Se o método determinar que o valor é muito pequeno, um valor dependente de modelo será especificado. Se for zero, um valor padrão de 4 será especificado.

</dd> <dt>

*MaxSubdiv* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Nível máximo de subdivisão de uma face que será usada na amostragem adaptável.

</dd> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída. Esse buffer deve ter o número correto de canais de cores alocados para a simulação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
