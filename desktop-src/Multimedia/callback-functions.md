---
title: Funções de retorno de chamada
description: Funções de retorno de chamada
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- drivers instaláveis, funções de retorno de chamada
- drivers instaláveis, função DriverCallback
- drivers instaláveis, eventos
- Função DriverCallback
- DRV_OPEN mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e23f933567d125dd07f81047ea8868c12f41ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823747"
---
# <a name="callback-functions"></a><span data-ttu-id="51336-108">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="51336-108">Callback Functions</span></span>

<span data-ttu-id="51336-109">Os drivers instaláveis podem notificar o aplicativo, a janela ou a tarefa que abriu a instância específica sobre eventos usando a função [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) .</span><span class="sxs-lookup"><span data-stu-id="51336-109">Installable drivers can notify the application, window, or task that opened the given instance about events by using the [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) function.</span></span> <span data-ttu-id="51336-110">Essa função fornece ao driver o meio de retornar informações a um aplicativo ou DLL enquanto continua a processar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="51336-110">This function gives the driver the means to return information to an application or DLL while continuing to process a request.</span></span>

<span data-ttu-id="51336-111">Se um driver oferecer suporte a funções de retorno de chamada, o aplicativo ou DLL que abre a instância do deve fornecer um valor esse é o endereço de uma função de retorno de chamada, um identificador de janela ou um identificador de tarefa.</span><span class="sxs-lookup"><span data-stu-id="51336-111">If a driver supports callback functions, the application or DLL that opens the instance must supply a value this is either the address of a callback function, a window handle, or a task handle.</span></span> <span data-ttu-id="51336-112">Esse valor e um sinalizador que identifica o tipo do valor são normalmente passados em uma estrutura apontada pelo segundo parâmetro da mensagem de [**\_ abertura do drv**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="51336-112">This value and a flag identifying the type of the value are typically passed in a structure pointed to by the second parameter of the [**DRV\_OPEN**](drv-open.md) message.</span></span>

 

 