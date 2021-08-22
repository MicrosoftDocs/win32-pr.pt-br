---
description: Calcula a contribuição de iluminação direta para objetos 3D em que o radiance de origem é representado por uma aproximação de SH (spherical) usando amostragem adaptável.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: Método ID3DXPRTEngine::ComputeDirectLightingSHAdaptive (D3DX9Mesh.h)
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
ms.openlocfilehash: 991337b31b10c39cccb622c2838bd53bcb25ad534ae8f896b6ec8f4842072de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801276"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>Método ID3DXPRTEngine::ComputeDirectLightingSHAdaptive

Calcula a contribuição de iluminação direta para objetos 3D em que o radiance de origem é representado por uma aproximação de SH (spherical) usando amostragem adaptável. Esse método gera novos vértices e faces na malha para aproximar com mais precisão o sinal de PRT (transferência de radiance pré-comutada).

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

*Ordem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordem da avaliação de SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes orderâmicos. O grau da avaliação é Order - 1.

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

Ponteiro para um objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) saída. Esse buffer deve ter o número adequado de canais de cores alocados para a simulação.

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

 

 
