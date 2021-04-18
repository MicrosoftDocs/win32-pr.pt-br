---
title: Função D3DX12ParsePipelineStream (D3dx12. h)
description: Analisa uma descrição de fluxo de estado de pipeline, chamando um retorno de chamada definido pelo usuário para cada instância de subobjeto analisada.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- Função D3DX12ParsePipelineStream
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814596"
---
# <a name="d3dx12parsepipelinestream-function"></a>Função D3DX12ParsePipelineStream

Analisa uma descrição de fluxo de estado de pipeline, chamando um retorno de chamada definido pelo usuário para cada instância de subobjeto analisada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Desc* \[ referência\]
</dt> <dd>

Tipo: **const [**D3D12 \_ pipeline \_ State \_ Stream \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

A descrição do fluxo de estado do pipeline para analisar.

</dd> <dt>

*pCallbacks* 
</dt> <dd>

Tipo: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

Uma estrutura que especifica os retornos de chamada a serem chamados para cada tipo de subobjeto e retornos de chamada adicionais para chamar no caso de um erro de análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Esse método retorna um erro HRESULT Success (**S \_ OK** ou **E \_ INVALIDARG** se um tipo de subobjeto desconhecido for encontrado, se a descrição do fluxo estiver vazia, nula ou contiver subobjetos duplicados (incluindo subobjetos derivados) ou se *pCallbacks* for nulo. Em cada caso em que E \_ INVALIDARG é retornado, um retorno de chamada correspondente é chamado primeiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





