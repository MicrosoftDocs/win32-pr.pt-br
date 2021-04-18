---
description: Estruturas SOCKADDR e suposições de ordenação de bytes no Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Suposições de ordenação de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814105"
---
# <a name="byte-ordering-assumptions"></a><span data-ttu-id="18106-103">Suposições de ordenação de bytes</span><span class="sxs-lookup"><span data-stu-id="18106-103">Byte Ordering Assumptions</span></span>

<span data-ttu-id="18106-104">Um provedor de serviços deve tratar todos os componentes [**SOCKADDR**](sockaddr-2.md) exclusivos do parâmetro de família de endereços como se eles estivessem na ordem de bytes de rede e o parâmetro de família de endereços como na ordem de bytes do computador local.</span><span class="sxs-lookup"><span data-stu-id="18106-104">A service provider should treat all [**sockaddr**](sockaddr-2.md) components exclusive of the address family parameter as if they are in the network byte order, and the address family parameter as in the local computer's byte order.</span></span> <span data-ttu-id="18106-105">É responsabilidade do aplicativo Winsock garantir que os endereços contidos em estruturas **SOCKADDR** sejam organizados corretamente.</span><span class="sxs-lookup"><span data-stu-id="18106-105">It is the Winsock application's responsibility to make sure that addresses contained in **sockaddr** structures are properly arranged.</span></span> <span data-ttu-id="18106-106">A API do Winsock fornece várias rotinas de conversão para simplificar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="18106-106">The Winsock API provides a number of conversion routines to simplify this task.</span></span> <span data-ttu-id="18106-107">Atualmente, essas rotinas entendem a conversão entre a ordem de bytes naturais do host local e a ordenação de bytes de rede big-endian ou little-endian.</span><span class="sxs-lookup"><span data-stu-id="18106-107">Currently these routines understand conversion between the local host's natural byte order and either big-Endian or little-Endian network byte ordering.</span></span> <span data-ttu-id="18106-108">A arquitetura do Winsock pode dar suporte a outros esquemas de ordenação de bytes no futuro.</span><span class="sxs-lookup"><span data-stu-id="18106-108">The Winsock architecture can support other byte ordering schemes in the future.</span></span>

 

 



