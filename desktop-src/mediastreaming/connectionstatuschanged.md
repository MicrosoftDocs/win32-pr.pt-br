---
title: Evento ConnectionStatusChanged
description: Ocorre quando o status da conexão de rede do dispositivo é alterado.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- API de streaming de mídia de evento ConnectionStatusChanged
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640965"
---
# <a name="connectionstatuschanged-event"></a>Evento ConnectionStatusChanged

Ocorre quando o status da conexão de rede do dispositivo é alterado.

## <a name="syntax"></a>Sintaxe


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) usando o método [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) . Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .

 

 