---
title: Função D3DPERF_SetMarker
description: Marque um evento instantâneo. O PIX pode usar esse evento para disparar uma ação.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104365698"
---
# <a name="d3dperf_setmarker-function"></a>Função D3DPERF_SetMarker

Marque um evento instantâneo. O PIX pode usar esse evento para disparar uma ação.

## <a name="syntax"></a>Sintaxe

```cpp
void WINAPI D3DPERF_SetMarker(
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

Os eventos de usuário instantâneos não têm nenhum colchete ou outro evento de grupo. Por exemplo, quando o usuário aciona uma arma em um jogo, um evento *acionado por captura* pode ser criado por uma chamada **D3DPERF_SetMarker** . Para agrupar vários eventos em um único nome definido pelo usuário, use **D3DPERF_BeginEvent** e **D3DPERF_EndEvent** em vez de **D3DPERF_SetMarker**.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9. h |
| **Biblioteca** | d3d9. lib |
| **DLL** | d3d9.dll |