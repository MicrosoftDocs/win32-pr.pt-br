---
description: O agente de rede DDE inicia o DDE de rede se detectar atividade DDE de rede local.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Agente DDE de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784184"
---
# <a name="network-dde-agent"></a><span data-ttu-id="07033-103">Agente DDE de rede</span><span class="sxs-lookup"><span data-stu-id="07033-103">Network DDE Agent</span></span>

<span data-ttu-id="07033-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="07033-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="07033-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="07033-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="07033-106">O agente de rede DDE inicia o DDE de rede se detectar atividade DDE de rede local.</span><span class="sxs-lookup"><span data-stu-id="07033-106">The network DDE agent starts network DDE if it detects local network DDE activity.</span></span> <span data-ttu-id="07033-107">Ele não detecta um cliente remoto tentando se conectar.</span><span class="sxs-lookup"><span data-stu-id="07033-107">It does not detect a remote client trying to connect.</span></span> <span data-ttu-id="07033-108">Portanto, antes que qualquer cliente possa se conectar com êxito, a rede DDE deve ser iniciada no computador servidor.</span><span class="sxs-lookup"><span data-stu-id="07033-108">Therefore, before any client can successfully connect, network DDE must be started on the server computer.</span></span> <span data-ttu-id="07033-109">Observe que o DDE de rede não é iniciado por padrão.</span><span class="sxs-lookup"><span data-stu-id="07033-109">Note that network DDE is not started by default.</span></span> <span data-ttu-id="07033-110">Para iniciar o DDE de rede, execute NETDDE.EXE.</span><span class="sxs-lookup"><span data-stu-id="07033-110">To start network DDE, run NETDDE.EXE.</span></span> <span data-ttu-id="07033-111">Esse arquivo está localizado no seu diretório do Windows.</span><span class="sxs-lookup"><span data-stu-id="07033-111">This file is located in your Windows directory.</span></span>

<span data-ttu-id="07033-112">O agente DDE de rede também inicia os aplicativos necessários para o DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="07033-112">The network DDE agent also starts the applications necessary for network DDE.</span></span> <span data-ttu-id="07033-113">Depois que o DDE de rede é iniciado, as conversas DDE são controladas por meio de uma janela DDE de rede associada a um dos aplicativos DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="07033-113">After network DDE is started, DDE conversations are controlled through a network DDE window associated with one of the network DDE applications.</span></span> <span data-ttu-id="07033-114">Esse aplicativo atua como um proxy.</span><span class="sxs-lookup"><span data-stu-id="07033-114">This application acts as a proxy.</span></span> <span data-ttu-id="07033-115">Ele se comunica com todos os aplicativos DDE locais e remotos.</span><span class="sxs-lookup"><span data-stu-id="07033-115">It communicates with all local and remote DDE applications.</span></span>

 

 



