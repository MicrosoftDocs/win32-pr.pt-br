---
description: Usa a GPU para calcular a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica (SH) esférica. A computação da iluminação na GPU geralmente será muito mais rápida do que na CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'Método ID3DXPRTEngine:: ComputeDirectLightingSHGPU (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14dc76cb8ac3875101c42beb581c7eb2b96eb7511c85e7f76cd034658afcca3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985576"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>Método ID3DXPRTEngine:: ComputeDirectLightingSHGPU

Usa a GPU para calcular a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica (SH) esférica. A computação da iluminação na GPU geralmente será muito mais rápida do que na CPU.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para o objeto de dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usado para executar a simulação na GPU. O dispositivo deve dar suporte a sombreadores do [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel.

> [!Note]  
> As funções de retorno de chamada não devem usar o objeto de dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usado pelo simulador de GPU.

 

</dd> <dt>

*Sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Parâmetro de simulação de GPU que define a resolução da sombra z-buffer. Deve ser definido como um dos valores constantes de [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md). Para especificar uma simulação de precisão mais alta, o \_ valor de Highquality D3DXSHGPUSIMOPT pode ser combinado com um dos \_ valores SHADOWRESxxx D3DXSHGPUSIMOPT.

</dd> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*ZBias* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Tendência na direção normal.

</dd> <dt>

*ZAngleBias* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Tendência na direção normal, dimensionada por um menos o cosseno do ângulo com o raio de luz.

</dd> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Esse buffer deve ter o número correto de canais de cores alocados para a simulação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Nesse método, o albedo não é multiplicado pelo sinal luminoso e apenas a luz de entrada é integrada ao simulador. Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.

Chame [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor de PRT (transferência de radiante) precomputado pelo albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
