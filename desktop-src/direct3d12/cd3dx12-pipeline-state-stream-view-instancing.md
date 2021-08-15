---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING (D3dx12. h)
description: Uma estrutura auxiliar usada para encapsular uma estrutura de [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) . Permite que os sombreadores sejam renderizados em várias exibições com uma única chamada de desenho; útil para a visão de estéreo ou geração de cubemap.
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 6bf5d69232f9cf61e7b650df1f53229eabff4e0a0199ef5ec804e6d592855a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261757"
---
# <a name="cd3dx12_pipeline_state_stream_view_instancing-structure"></a>Estrutura de CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING

Uma estrutura auxiliar usada para encapsular uma estrutura de [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) . Permite que os sombreadores sejam renderizados em várias exibições com uma única chamada de desenho; útil para a visão de estéreo ou geração de cubemap.

## <a name="syntax"></a>Syntax

```cpp
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_VIEW_INSTANCING_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VIEW_INSTANCING, CD3DX12_DEFAULT> CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING;
```

**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING** é uma `typedef` especialização do modelo de [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) .

## <a name="members"></a>Membros

Consulte [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) e [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md).

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md)
* [D3D12_PIPELINE_STATE_SUBOBJECT_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
