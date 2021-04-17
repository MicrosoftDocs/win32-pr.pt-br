---
title: Função D3DPERF_SetRegion
description: Marque uma série de quadros com a cor e o nome especificados no arquivo PIXRun. Atualmente, essa função não tem suporte no PIX.
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
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "105812137"
---
# <a name="d3dperf_setregion-function"></a>Função D3DPERF_SetRegion

Marque uma série de quadros com a cor e o nome especificados no arquivo PIXRun. Atualmente, essa função não tem suporte no PIX.

## <a name="syntax"></a>Sintaxe

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>Parâmetros

`col`

Cor do evento. Essa é a cor para exibir o evento no modo de exibição de evento.

`wszName`

Nome do evento.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Para facilitar a análise, o programa de destino pode usar cores para marcar cada nível de um programa de destino.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9. h |
| **Biblioteca** | d3d9. lib |
| **DLL** | d3d9.dll |