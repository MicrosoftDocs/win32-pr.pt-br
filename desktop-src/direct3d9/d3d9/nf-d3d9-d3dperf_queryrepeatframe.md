---
title: Função D3DPERF_QueryRepeatFrame
description: Determine se um criador de perfil de desempenho está solicitando que o quadro atual seja reenviado ao Direct3D para análise de desempenho. Atualmente, essa função não tem suporte no PIX.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "103640240"
---
# <a name="d3dperf_queryrepeatframe-function"></a>Função D3DPERF_QueryRepeatFrame

Determine se um criador de perfil de desempenho está solicitando que o quadro atual seja reenviado ao Direct3D para análise de desempenho. Atualmente, essa função não tem suporte no PIX.

## <a name="syntax"></a>Sintaxe

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Retornar valor

Se o valor de retorno for TRUE, o chamador deverá repetir a mesma sequência de chamadas. Se for FALSE, o chamador deverá continuar.

## <a name="remarks"></a>Comentários

A função deve ser chamada imediatamente após **IDirect3DDevice9::P reenviado** é chamado.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9. h |
| **Biblioteca** | d3d9. lib |
| **DLL** | d3d9.dll |