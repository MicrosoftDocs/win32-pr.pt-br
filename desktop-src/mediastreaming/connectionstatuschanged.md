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
# <a name="connectionstatuschanged-event"></a><span data-ttu-id="17863-104">Evento ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="17863-104">ConnectionStatusChanged event</span></span>

<span data-ttu-id="17863-105">Ocorre quando o status da conexão de rede do dispositivo é alterado.</span><span class="sxs-lookup"><span data-stu-id="17863-105">Occurs when the device’s network connection status changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="17863-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17863-106">Syntax</span></span>


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a><span data-ttu-id="17863-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17863-107">Parameters</span></span>

<span data-ttu-id="17863-108">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="17863-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17863-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17863-109">Return value</span></span>

<span data-ttu-id="17863-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="17863-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17863-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="17863-111">Remarks</span></span>

<span data-ttu-id="17863-112">Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) usando o método [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="17863-112">To handle notifications from this event, register a [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function using the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method.</span></span> <span data-ttu-id="17863-113">Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="17863-113">To unregister the event handler, use the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

 

 