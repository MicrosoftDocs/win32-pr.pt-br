---
title: D3DPERF_GetStatus função
description: Determine o estado atual do profiler do programa de destino.
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 78ff9eda9ab224faf4b2a117f6230e3361664bbfea35d8b2a8484ba7f5ab764a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805741"
---
# <a name="d3dperf_getstatus-function"></a>D3DPERF_GetStatus função

Determine o estado atual do profiler do programa de destino.

## <a name="syntax"></a>Sintaxe

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>Valor retornado

Um valor não zero quando o SEGMENT está criação de perfil do programa de destino; caso contrário, zero.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9.h |
| **Biblioteca** | d3d9.lib |
| **DLL** | d3d9.dll |