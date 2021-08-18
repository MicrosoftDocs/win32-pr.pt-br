---
title: Interface ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Uma interface que representa uma coleção de analisador e retornos de chamada de erro usados pela função auxiliar D3DX12parsePipelineStream.
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- Interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, descrita
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f83e0987009e60d5e207a9531cc4809f6cfcfbd5b50360a583df8cb0c01898f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733739"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a>Interface ID3DX12PipelineParserCallbacks

Uma interface que representa uma coleção de analisador e retornos de chamada de erro usados pela função auxiliar [**D3DX12parsePipelineStream.**](d3dx12parsepipelinestream.md)

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX12PipelineParserCallbacks** tem esses métodos.



| Método                                                                                    | Descrição                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BlendStateCb**](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | Chama o retorno de chamada de subobjeto de descrição de estado de combinação de um objeto que implementa essa interface.<br/>                                                                 |
| [**CachedPSOCb**](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | Chama o retorno de chamada do subobjeto PSO (Objeto de Estado do Pipeline) armazenado em cache de um objeto que implementa essa interface.<br/>                                                      |
| [**CSCb**](id3dx12pipelineparsercallbacks-cscb.md)                                       | Chama o retorno de chamada de subobjeto do sombreador de computação de um objeto que implementa essa interface.<br/>                                                                          |
| [**DepthStencilState1Cb**](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | Chama o retorno de chamada de subobjeto de estêncil de profundidade ([**D3D12 \_ DEPTH \_ \_ STENCIL DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) de um objeto que implementa essa interface.<br/> |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | Chama o retorno de chamada de subobjeto de formato de valor de estêncil de profundidade de um objeto que implementa essa interface.<br/>                                                              |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | Chama o retorno de chamada de subobjeto de estado de estêncil de profundidade de um objeto que implementa essa interface.<br/>                                                                     |
| [**DSCb**](id3dx12pipelineparsercallbacks-dscb.md)                                       | Chama o retorno de chamada de subobjeto do sombreador de domínio de um objeto que implementa essa interface.<br/>                                                                           |
| [**ErrorBadInputParameter**](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | Chama o retorno de chamada de erro de parâmetro de entrada ruim de um objeto que implementa essa interface.<br/>                                                                         |
| [**ErrorDuplicateSubobject**](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | Chama o retorno de chamada de erro de subobjeto duplicado de um objeto que implementa essa interface.<br/>                                                                         |
| [**ErrorUnknownSubobject**](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | Chama o retorno de chamada de erro de subobjeto desconhecido de um objeto que implementa essa interface.<br/>                                                                           |
| [**FlagsCb**](id3dx12pipelineparsercallbacks-flagscb.md)                                 | Chama o retorno de chamada de subobjeto de sinalizadores de um objeto que implementa essa interface.<br/>                                                                                   |
| [**GSCb**](id3dx12pipelineparsercallbacks-gscb.md)                                       | Chama o retorno de chamada de subobjeto do sombreador de geometria de um objeto que implementa essa interface.<br/>                                                                         |
| [**HSCb**](id3dx12pipelineparsercallbacks-hscb.md)                                       | Chama o retorno de chamada do subobjeto do sombreador de chassi de um objeto que implementa essa interface.<br/>                                                                             |
| [**IBStripCutValueCb**](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | Chama o subobjeto de subobjeto de valor de recortar buffer de índice de um objeto que implementa essa interface.<br/>                                                            |
| [**InputLayoutCb**](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | Chama o retorno de chamada de subobjeto de layout de entrada de um objeto que implementa essa interface.<br/>                                                                            |
| [**NodemaskCb**](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | Chama o retorno de chamada de subobjeto nodemask de um objeto que implementa essa interface.<br/>                                                                                |
| [**PrimitiveTopologyTypeCb**](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | Chama o retorno de chamada de subobjeto do tipo topologia primitivo de um objeto que implementa essa interface.<br/>                                                                 |
| [**PSCb**](id3dx12pipelineparsercallbacks-pscb.md)                                       | Chama o retorno de chamada de subobjeto do sombreador de pixel de um objeto que implementa essa interface.<br/>                                                                            |
| [**RasterizerStateCb**](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | Chama o retorno de chamada de subobjeto de descrição do estado do rasterizador de um objeto que implementa essa interface.<br/>                                                            |
| [**RootSignatureCB**](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | Chama o retorno de chamada de subobjeto de assinatura raiz de um objeto que implementa essa interface.<br/>                                                                          |
| [**RTVFormatsCb**](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | Chama o retorno de chamada de subobjeto da matriz de formato de destino de renderização de um objeto que implementa essa interface.<br/>                                                              |
| [**SampleDescCb**](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | Chama o retorno de chamada de subobjeto de descrição de exemplo de um objeto que implementa essa interface.<br/>                                                                      |
| [**SampleMaskCb**](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | Chama o retorno de chamada de subobjeto de máscara de exemplo de um objeto que implementa essa interface.<br/>                                                                             |
| [**StreamOutputCb**](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | Chama o retorno de chamada de subobjeto de descrição de saída de fluxo de um objeto que implementa essa interface.<br/>                                                               |
| [**VSCb**](id3dx12pipelineparsercallbacks-vscb.md)                                       | Chama o subobjeto de subobjeto do sombreador de vértice de um objeto que implementa essa interface.<br/>                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces auxiliares para Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





