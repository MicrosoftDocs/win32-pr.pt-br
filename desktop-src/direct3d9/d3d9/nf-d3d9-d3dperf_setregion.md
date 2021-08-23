---
title: D3DPERF_SetRegion função
description: Marque uma série de quadros com a cor e o nome especificados no arquivo PROTOCOLRun. Atualmente, não há suporte para essa função por MEIO DEM.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 05884fe8a3b104588a941dcaf3089a1c0f6f8eab4f4a01e143470f73454ad4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989256"
---
# <a name="d3dperf_setregion-function"></a>D3DPERF_SetRegion função

Marque uma série de quadros com a cor e o nome especificados no arquivo PROTOCOLRun. Atualmente, não há suporte para essa função por MEIO DEM.

## <a name="syntax"></a>Sintaxe

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>Parâmetros

`col`

Cor do evento. Essa é a cor para exibir o evento na exibição de evento.

`wszName`

Nome do evento.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Para facilitar a análise, o programa de destino pode usar a cor para marcar cada nível de um programa de destino.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9.h |
| **Biblioteca** | d3d9.lib |
| **DLL** | d3d9.dll |