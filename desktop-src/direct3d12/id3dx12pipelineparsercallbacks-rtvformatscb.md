---
title: Método ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de matriz de formato de destino de renderização de um objeto que implementa essa interface.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Método RTVFormatsCb
- Método RTVFormatsCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método RTVFormatsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790388"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a>Método ID3DX12PipelineParserCallbacks:: RTVFormatsCb

Chama o retorno de chamada de subobjeto de matriz de formato de destino de renderização de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RTVFormats* \[ referência\]
</dt> <dd>

Tipo: **[**matriz de \_ \_ formato \_ const D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**

Detalhes do subobjeto de matriz de formato de destino de renderização analisado de um fluxo de estado de pipeline.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Não retorna nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces auxiliares para Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**\_Matriz de \_ formato D3D12 RT \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





