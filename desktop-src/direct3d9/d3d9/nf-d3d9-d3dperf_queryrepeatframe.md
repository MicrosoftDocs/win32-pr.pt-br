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
ms.openlocfilehash: dbc46ff05b6fa1846bb0e1ffc1fca928ca1d68ee38a43708c77a109b61a405da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751236"
---
# <a name="d3dperf_queryrepeatframe-function"></a>Função D3DPERF_QueryRepeatFrame

Determine se um criador de perfil de desempenho está solicitando que o quadro atual seja reenviado ao Direct3D para análise de desempenho. Atualmente, essa função não tem suporte no PIX.

## <a name="syntax"></a>Sintaxe

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Valor retornado

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