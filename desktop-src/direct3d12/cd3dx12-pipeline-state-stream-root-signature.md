---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever a assinatura raiz como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccddd5663b6a079656823efed4cb48b3183d88d0688149c7ae05d96e8dc1cdd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530696"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a>\_Estrutura de \_ \_ \_ assinatura raiz do fluxo de estado do pipeline CD3DX12 \_

Uma estrutura auxiliar usada para descrever a assinatura raiz como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ \_ Assinatura raiz do fluxo de estado \_ do pipeline CD3DX12 \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ assinatura raiz do fluxo de estado do pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ Assinatura raiz do fluxo de estado do pipeline CD3DX12 \_ (ID3D12RootSignature \* const &i)**
</dt> <dd>

Cria uma nova instância de uma \_ assinatura raiz do fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto de **\_ \_ \_ \_ \_ \_ assinatura raiz do tipo** de subobjeto do estado do pipeline D3D12 e dados de subobjeto copiados de *i*, uma estrutura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> <dt>

**Operator = (ID3D12RootSignature \* const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**constante ID3D12RootSignature \* () de operador**
</dt> <dd>

Conversão implícita em um ponteiro de estrutura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ \_ A assinatura raiz do fluxo de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

