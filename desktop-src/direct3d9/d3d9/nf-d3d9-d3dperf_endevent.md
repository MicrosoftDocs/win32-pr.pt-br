---
title: Função D3DPERF_EndEvent
description: Marca o final de um evento definido pelo usuário. O PIX pode usar esse evento para disparar uma ação.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: bd12780dfdfcb86e83495ae877d8debf1e768517826329ccee8d40ffaa88fbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989246"
---
# <a name="d3dperf_endevent-function"></a>Função D3DPERF_EndEvent

Marca o final de um evento definido pelo usuário. O PIX pode usar esse evento para disparar uma ação.

## <a name="syntax"></a>Sintaxe

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Valor retornado

O nível da hierarquia na qual o evento está terminando. Se ocorrer um erro, esse valor será negativo.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9. h |
| **Biblioteca** | d3d9. lib |
| **DLL** | d3d9.dll |