---
title: Função D3DPERF_GetStatus
description: Determine o estado atual do criador de perfil do programa de destino.
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
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104293836"
---
# <a name="d3dperf_getstatus-function"></a>Função D3DPERF_GetStatus

Determine o estado atual do criador de perfil do programa de destino.

## <a name="syntax"></a>Sintaxe

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>Retornar valor

Um valor diferente de zero quando o PIX está criando o perfil do programa de destino; caso contrário, zero.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9. h |
| **Biblioteca** | d3d9. lib |
| **DLL** | d3d9.dll |