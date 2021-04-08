---
description: O provedor de registro do sistema tenta enviar uma notificação para cada evento que ocorre.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Recebendo eventos do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010765"
---
# <a name="receiving-registry-events"></a><span data-ttu-id="2a682-103">Recebendo eventos do registro</span><span class="sxs-lookup"><span data-stu-id="2a682-103">Receiving Registry Events</span></span>

<span data-ttu-id="2a682-104">O provedor de registro do sistema tenta enviar uma notificação para cada evento que ocorre.</span><span class="sxs-lookup"><span data-stu-id="2a682-104">The System Registry provider attempts to send one notification for every event that occurs.</span></span> <span data-ttu-id="2a682-105">No entanto, o provedor de registro do sistema não garante que o consumidor receberá um ou todos os eventos.</span><span class="sxs-lookup"><span data-stu-id="2a682-105">However, the System Registry provider does not guarantee that the consumer will receive any or all events.</span></span> <span data-ttu-id="2a682-106">A exceção é que o provedor de registro do sistema garante que um consumidor receberá uma notificação para cada registro de evento.</span><span class="sxs-lookup"><span data-stu-id="2a682-106">The exception is that the System Registry provider does ensure that a consumer will receive one notification for each event registration.</span></span>

<span data-ttu-id="2a682-107">Por exemplo, suponha que um consumidor se registre em dois eventos de alteração de árvore, solicitando notificação para instâncias de [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) .</span><span class="sxs-lookup"><span data-stu-id="2a682-107">For example, suppose a consumer registers for two tree change events, requesting notification for [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) instances.</span></span> <span data-ttu-id="2a682-108">Cada registro tem o mesmo valor de Hive (subárvore), mas um valor diferente de RootPath.</span><span class="sxs-lookup"><span data-stu-id="2a682-108">Each registration has the same Hive (subtree) value but a different RootPath value.</span></span> <span data-ttu-id="2a682-109">Se as chaves em ambos os caminhos forem alteradas várias vezes, o provedor de registro do sistema garante que o consumidor receberá uma notificação para cada caminho.</span><span class="sxs-lookup"><span data-stu-id="2a682-109">If keys in both paths change multiple times, the System Registry provider guarantees that the consumer will receive a notification for each path.</span></span> <span data-ttu-id="2a682-110">Dependendo do tempo de resposta do registro e do provedor de registro do sistema, o consumidor pode receber tantas notificações quanto houve ocorrências de eventos.</span><span class="sxs-lookup"><span data-stu-id="2a682-110">Depending on the response time of the registry and the System Registry provider, the consumer may receive as many notifications as there were occurrences of events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a682-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a682-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a682-112">Registrando para eventos de registro do sistema</span><span class="sxs-lookup"><span data-stu-id="2a682-112">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> </dl>

 

 
