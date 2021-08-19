---
title: Evento ConnectionStatusChanged
description: Ocorre quando o status de conexão de rede do dispositivo muda.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- API de Streaming de Mídia do evento ConnectionStatusChanged
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ccc19c71b56977a77ac5ec05448ea72eaff79d9e96b42f4f297d7046079f571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060426"
---
# <a name="connectionstatuschanged-event"></a>Evento ConnectionStatusChanged

Ocorre quando o status de conexão de rede do dispositivo muda.

## <a name="syntax"></a>Sintaxe


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Parâmetros

Esse evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para manipular notificações desse evento, registre uma função de manipulador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) usando o [**método add \_ ConnectionStatusChanged.**](ibasicdevice-add-connectionstatuschanged.md) Para remover o registro do manipulador de eventos, use [**o \_ método remove ConnectionStatusChanged.**](ibasicdevice-remove-connectionstatuschanged.md)

 

 