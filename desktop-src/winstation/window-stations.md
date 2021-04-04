---
title: Estações de janela
description: Uma estação de janela contém uma área de transferência, uma tabela Atom e um ou mais objetos desktop. Cada objeto de estação de janela é um objeto protegível. Quando uma estação de janela é criada, ela é associada ao processo de chamada e atribuída à sessão atual.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- objetos de estação de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007720"
---
# <a name="window-stations"></a><span data-ttu-id="df13e-106">Estações de janela</span><span class="sxs-lookup"><span data-stu-id="df13e-106">Window Stations</span></span>

<span data-ttu-id="df13e-107">Uma *estação de janela* contém uma área de transferência, uma tabela Atom e um ou mais objetos [Desktop](desktops.md) .</span><span class="sxs-lookup"><span data-stu-id="df13e-107">A *window station* contains a clipboard, an atom table, and one or more [desktop](desktops.md) objects.</span></span> <span data-ttu-id="df13e-108">Cada objeto de estação de janela é um objeto protegível.</span><span class="sxs-lookup"><span data-stu-id="df13e-108">Each window station object is a securable object.</span></span> <span data-ttu-id="df13e-109">Quando uma estação de janela é criada, ela é associada ao processo de chamada e atribuída à sessão atual.</span><span class="sxs-lookup"><span data-stu-id="df13e-109">When a window station is created, it is associated with the calling process and assigned to the current session.</span></span>

<span data-ttu-id="df13e-110">A *estação de janela interativa* é a única estação de janela que pode exibir uma interface do usuário ou receber entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="df13e-110">The *interactive window station* is the only window station that can display a user interface or receive user input.</span></span> <span data-ttu-id="df13e-111">Ele é atribuído à sessão de logon do usuário interativo e contém o teclado, o mouse e o dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="df13e-111">It is assigned to the logon session of the interactive user, and contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="df13e-112">Ele é sempre denominado "WinSta0".</span><span class="sxs-lookup"><span data-stu-id="df13e-112">It is always named "WinSta0".</span></span> <span data-ttu-id="df13e-113">Todas as outras estações de janela são não interativas, o que significa que elas não podem exibir uma interface do usuário ou receber entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="df13e-113">All other window stations are noninteractive, which means they cannot display a user interface or receive user input.</span></span>

<span data-ttu-id="df13e-114">Quando um usuário faz logon em um computador usando Serviços de Área de Trabalho Remota, uma sessão é iniciada para o usuário.</span><span class="sxs-lookup"><span data-stu-id="df13e-114">When a user logs on to a computer using Remote Desktop Services, a session is started for the user.</span></span> <span data-ttu-id="df13e-115">Cada sessão é associada a sua própria estação de janela interativa chamada "WinSta0".</span><span class="sxs-lookup"><span data-stu-id="df13e-115">Each session is associated with its own interactive window station named "WinSta0".</span></span> <span data-ttu-id="df13e-116">Para obter mais informações, consulte [área de trabalho remota sessões](/windows/desktop/TermServ/terminal-services-sessions).</span><span class="sxs-lookup"><span data-stu-id="df13e-116">For more information, see [Remote Desktop Sessions](/windows/desktop/TermServ/terminal-services-sessions).</span></span>

<span data-ttu-id="df13e-117">Para obter mais informações sobre estações de janela, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="df13e-117">For more information on window stations, see the following topics:</span></span>

-   [<span data-ttu-id="df13e-118">Estação de janela e criação de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="df13e-118">Window Station and Desktop Creation</span></span>](window-station-and-desktop-creation.md)
-   [<span data-ttu-id="df13e-119">Processar conexão com uma estação de janela</span><span class="sxs-lookup"><span data-stu-id="df13e-119">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
-   [<span data-ttu-id="df13e-120">Segurança de estação de janela e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="df13e-120">Window Station Security and Access Rights</span></span>](window-station-security-and-access-rights.md)

 

 