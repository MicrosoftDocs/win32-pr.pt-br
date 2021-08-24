---
title: Método ID3DX12PipelineParserCallbacks RootSignatureCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de assinatura raiz de um objeto que implementa essa interface.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- Método RootSignatureCb
- Método RootSignatureCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método RootSignatureCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52b284a1f44ae1f77c80788b1af21cf29ba480881e82feac38bfccdba6e8e8ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792146"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a>Método ID3DX12PipelineParserCallbacks:: RootSignatureCb

Chama o retorno de chamada de subobjeto de assinatura raiz de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RootSignature* 
</dt> <dd>

Tipo: **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***

Detalhes do subobjeto de assinatura raiz analisado a partir de um fluxo de estado do pipeline.

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

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

