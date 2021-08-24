---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12.h)
description: Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12.h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 estrutura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f04064a7ab4a7ca100e48da2446501d4415b693ce6abdf213f121952cc8f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632517"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>Estrutura \_ \_ \_ \_ \_ STENCIL1 DE PROFUNDIDADE DE FLUXO DE ESTADO DO PIPELINE CD3DX12

Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL1**
</dt> <dd>

Cria uma nova instância, não reinicializada, de uma CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1 const &i)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL1, inicializado com um \_ \_ tipo de \_ \_ \_ subobjeto **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE DEPTH \_ \_ STENCIL1** e dados de subobjeto copiados de *i*, uma estrutura [**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1.**](cd3dx12-depth-stencil-desc1.md)

</dd> <dt>

**operator=(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1 const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operador CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1() const**
</dt> <dd>

Conversão implícita em uma [**estrutura CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1.**](cd3dx12-depth-stencil-desc1.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL1 é uma especialização typedef do modelo \_ \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT DE**](cd3dx12-pipeline-state-stream-subobject.md) FLUXO DE ESTADO DO PIPELINE CD3DX12 e é definido da seguinte forma:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**TIPO DE \_ \_ \_ SUBOBJETO DE ESTADO DO PIPELINE D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

