---
title: Função D3DPERF_BeginEvent
description: Marca o início de um evento definido pelo usuário. O PIX pode usar esse evento para disparar uma ação.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104365697"
---
# <a name="d3dperf_beginevent-function"></a>Função D3DPERF_BeginEvent

Marca o início de um evento definido pelo usuário. O PIX pode usar esse evento para disparar uma ação.

## <a name="syntax"></a>Sintaxe

```cpp
int WINAPI D3DPERF_BeginEvent(
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

O nível de base zero da hierarquia em que esse evento está sendo iniciado. Se ocorrer um erro, o valor de retorno será negativo.

## <a name="remarks"></a>Comentários

Os eventos definidos pelo usuário agrupam outros eventos de forma que sejam significativos ao programa de destino para que possam ser melhor representados em ferramentas de criação de perfil de desempenho. Por exemplo, um evento *desenhar espaçamento* pode ser um número de chamadas Direct3D que lidam com o desenho de uma área de controle em um jogo. Os eventos podem ser aninhados.

Cada chamada de **D3DPERF_BeginEvent** deve ter uma chamada de **D3DPERF_EndEvent** correspondente. Os eventos instantâneos (que não têm outros eventos) devem ser rotulados usando **D3DPERF_SetMarker** em vez de **D3DPERF_BeginEvent** e **D3DPERF_EndEvent**.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | d3d9. h |
| **Biblioteca** | d3d9. lib |
| **DLL** | d3d9.dll |