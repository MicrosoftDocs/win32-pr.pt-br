---
title: Endereços IP e nomes de computador
description: Não é seguro pressupor que o nome do computador ou o endereço IP atribuído ao computador está associados um único usuário, pois vários usuários podem ser conectados simultaneamente a um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294413"
---
# <a name="ip-addresses-and-computer-names"></a><span data-ttu-id="c6848-103">Endereços IP e nomes de computador</span><span class="sxs-lookup"><span data-stu-id="c6848-103">IP addresses and computer names</span></span>

<span data-ttu-id="c6848-104">Vários usuários podem ser conectados simultaneamente a um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="c6848-104">Multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="c6848-105">Consequentemente, não é seguro supor que o nome do computador ou o endereço IP atribuído ao computador estejam associados a um único usuário.</span><span class="sxs-lookup"><span data-stu-id="c6848-105">Consequently, it is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user.</span></span> <span data-ttu-id="c6848-106">Isso é diferente de um ambiente Windows de usuário único, no qual apenas um usuário está conectado por vez.</span><span class="sxs-lookup"><span data-stu-id="c6848-106">This differs from a single-user Windows environment, in which only one user is logged on at a time.</span></span>

<span data-ttu-id="c6848-107">Os aplicativos que usam o nome do computador ou endereço IP para licenciamento ou como um meio de identificar uma iteração do aplicativo na rede não funcionarão corretamente em um ambiente Serviços de Área de Trabalho Remota, pois o nome do computador ou o endereço IP do servidor pode ser associado a muitos usuários.</span><span class="sxs-lookup"><span data-stu-id="c6848-107">Applications that use the computer name or IP address for licensing or as a means of identifying an iteration of the application on the network will not work properly in a Remote Desktop Services environment, because the server's computer name or IP address can be associated with many users.</span></span>

<span data-ttu-id="c6848-108">Em um ambiente de Serviços de Área de Trabalho Remota, cada terminal de cliente ou emulador de terminal tem um endereço IP e um nome de computador separados.</span><span class="sxs-lookup"><span data-stu-id="c6848-108">In a Remote Desktop Services environment, each client terminal or terminal emulator has a separate IP address and computer name.</span></span> <span data-ttu-id="c6848-109">Para recuperar o endereço IP e o nome do computador de um cliente, chame a função [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) .</span><span class="sxs-lookup"><span data-stu-id="c6848-109">To retrieve the IP address and computer name of a client, call the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span> <span data-ttu-id="c6848-110">Outras funções que recuperam esses endereços de rede e nomes de computador recuperam o nome e o endereço do servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="c6848-110">Other functions that retrieve these network addresses and computer names retrieve the name and address of the RD Session Host server.</span></span> <span data-ttu-id="c6848-111">Por exemplo, a função [**GetComputerNameEx devia**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) retorna o nome do computador do servidor.</span><span class="sxs-lookup"><span data-stu-id="c6848-111">For example, the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function returns the computer name of the server.</span></span>

 

 