---
title: Gerenciador de Conexões
description: Os clientes que pretendem desenvolver discadores personalizados usando a API do serviço de acesso remoto podem querer investigar o Gerenciador de conexões da Microsoft e o kit de administração do Gerenciador de conexões.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007176"
---
# <a name="connection-manager"></a><span data-ttu-id="45874-103">Gerenciador de Conexões</span><span class="sxs-lookup"><span data-stu-id="45874-103">Connection Manager</span></span>

<span data-ttu-id="45874-104">Os clientes que pretendem desenvolver discadores personalizados usando a API do serviço de acesso remoto podem querer investigar o Gerenciador de conexões da Microsoft e o kit de administração do Gerenciador de conexões.</span><span class="sxs-lookup"><span data-stu-id="45874-104">Customers who intend to develop custom dialers using the Remote Access Service API may want to investigate Microsoft Connection Manager and the Connection Manager Administration Kit.</span></span> <span data-ttu-id="45874-105">O Gerenciador de conexões é o cliente de acesso remoto gerenciado da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="45874-105">Connection Manager is Microsoft's managed remote access client.</span></span> <span data-ttu-id="45874-106">Ele permite que um administrador crie um pacote de configuração de acesso remoto para ser distribuído aos usuários remotos do administrador.</span><span class="sxs-lookup"><span data-stu-id="45874-106">It allows an administrator to build a remote access configuration package to be distributed to the administrator's remote users.</span></span> <span data-ttu-id="45874-107">Para obter mais informações sobre o Gerenciador de conexões e o kit de administração do Gerenciador de conexões, consulte a ajuda online do Microsoft Windows 2000 Server e sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="45874-107">For more information on Connection Manager and the Connection Manager Administration Kit, see the online help for Microsoft Windows 2000 Server and later operating systems.</span></span>

<span data-ttu-id="45874-108">Você pode encontrar o código-fonte para uma ação personalizada do Gerenciador de conexões de exemplo no SDK (Kit de desenvolvimento de software) completo da plataforma.</span><span class="sxs-lookup"><span data-stu-id="45874-108">You can find the source code for a sample Connection Manager custom action in the complete Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="45874-109">O SDK da plataforma pode ser baixado no [site da Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="45874-109">The Platform SDK can be downloaded at the [Microsoft Web site](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="45874-110">Após a instalação, o caminho para o código de exemplo é% install caminho% \\ Microsoft SDK \\ Samples \\ netds \\ RAS \\ ConnectionManager, em que% install caminho% designa o diretório de instalação base do SDK da plataforma (por exemplo, C: \\ arquivos de programas).</span><span class="sxs-lookup"><span data-stu-id="45874-110">After installation, the path to the sample code is %Install Path%\\Microsoft SDK\\Samples\\netds\\Ras\\ConnectionManager, where %Install Path% designates the base installation directory of the Platform SDK (for example, C:\\Program Files).</span></span>

<span data-ttu-id="45874-111">As ações personalizadas possibilitam que o cliente de acesso remoto execute ações específicas em vários pontos no processo de conexão.</span><span class="sxs-lookup"><span data-stu-id="45874-111">Custom actions make it possible for the remote access client to take specific actions at various points in the connection process.</span></span> <span data-ttu-id="45874-112">A ação personalizada demonstrada no exemplo ajusta automaticamente a configuração do servidor proxy para uma conexão com base no endereço do servidor da conexão.</span><span class="sxs-lookup"><span data-stu-id="45874-112">The custom action demonstrated in the sample automatically adjusts the proxy server configuration for a connection based on the connection's server address.</span></span> <span data-ttu-id="45874-113">Os clientes podem usar este exemplo como um ponto de partida para a criação de suas próprias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="45874-113">Customers can use this sample as a starting point for creating their own custom actions.</span></span>

 

 




