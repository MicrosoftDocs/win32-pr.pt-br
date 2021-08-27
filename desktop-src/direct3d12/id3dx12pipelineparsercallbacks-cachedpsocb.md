---
title: Método ID3DX12PipelineParserCallbacks CachedPSOCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto PSO (objeto de estado de pipeline) armazenado em cache de um objeto que implementa essa interface.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Método CachedPSOCb
- Método CachedPSOCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método CachedPSOCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb585a3c82b7e85e6653efee6b3a1bf050051fec5cef0a2c82f0645fef542d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807493"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a>Método ID3DX12PipelineParserCallbacks:: CachedPSOCb

Chama o retorno de chamada de subobjeto PSO (objeto de estado de pipeline) armazenado em cache de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CachedPSO* \[ referência\]
</dt> <dd>

Tipo: **const [**D3D12 \_ estado de \_ pipeline \_ armazenado em cache**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**

Detalhes do subobjeto de PSO (objeto de estado do Pipeline) em cache analisado a partir de um fluxo de estado do pipeline.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**\_Estado de pipeline armazenado em cache D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





