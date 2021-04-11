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
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104365699"
---
# <a name="d3dperf_endevent-function"></a>Função D3DPERF_EndEvent

Marca o final de um evento definido pelo usuário. O PIX pode usar esse evento para disparar uma ação.

## <a name="syntax"></a>Sintaxe

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Retornar valor

O nível da hierarquia na qual o evento está terminando. Se ocorrer um erro, esse valor será negativo.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9. h |
| **Biblioteca** | d3d9. lib |
| **DLL** | d3d9.dll |