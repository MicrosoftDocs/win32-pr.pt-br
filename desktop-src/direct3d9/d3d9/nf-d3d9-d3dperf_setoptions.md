---
title: Função D3DPERF_SetOptions
description: Defina as opções do criador de perfil especificadas pelo programa de destino.
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 579c07d8f93696e4e3c83b1e61c1ff5fca65e12b5a7cf0a5937a254ecc6dc306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805731"
---
# <a name="d3dperf_setoptions-function"></a>Função D3DPERF_SetOptions

Defina as opções do criador de perfil especificadas pelo programa de destino.

## <a name="syntax"></a>Sintaxe

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>Parâmetros

`dwOptions`

Opções de usuário reconhecíveis pelo PIX. Defina isso como 1 para notificar o PIX de que o programa de destino não dá permissão para ser criado.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9. h |
| **Biblioteca** | d3d9. lib |
| **DLL** | d3d9.dll |