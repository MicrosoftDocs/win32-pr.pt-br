---
title: Método ID3DX12PipelineParserCallbacks PSCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto do sombreador de pixel de um objeto que implementa essa interface.
ms.assetid: 3397B018-C26A-426F-88BB-89013BACBEEA
keywords:
- Método PSCb
- Método PSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método PSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c15b09598218259d5cdeedfb3453aaf2a4f669242ddb76e676093e81e0dd9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894566"
---
# <a name="id3dx12pipelineparsercallbackspscb-method"></a>ID3DX12PipelineParserCallbacks: método SCb de:P

Chama o retorno de chamada de subobjeto do sombreador de pixel de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void PSCb(
  [ref] const D3D12_SHADER_BYTECODE &PS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PS* \[ referência\]
</dt> <dd>

Tipo: **[**código de \_ \_ bytes do sombreador const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Detalhes do subobjeto do sombreador de pixel analisado a partir de um fluxo de estado do pipeline.

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

[**\_Código de bytes do sombreador D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





