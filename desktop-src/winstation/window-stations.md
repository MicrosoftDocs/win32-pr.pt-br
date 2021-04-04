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
# <a name="window-stations"></a>Estações de janela

Uma *estação de janela* contém uma área de transferência, uma tabela Atom e um ou mais objetos [Desktop](desktops.md) . Cada objeto de estação de janela é um objeto protegível. Quando uma estação de janela é criada, ela é associada ao processo de chamada e atribuída à sessão atual.

A *estação de janela interativa* é a única estação de janela que pode exibir uma interface do usuário ou receber entrada do usuário. Ele é atribuído à sessão de logon do usuário interativo e contém o teclado, o mouse e o dispositivo de vídeo. Ele é sempre denominado "WinSta0". Todas as outras estações de janela são não interativas, o que significa que elas não podem exibir uma interface do usuário ou receber entrada do usuário.

Quando um usuário faz logon em um computador usando Serviços de Área de Trabalho Remota, uma sessão é iniciada para o usuário. Cada sessão é associada a sua própria estação de janela interativa chamada "WinSta0". Para obter mais informações, consulte [área de trabalho remota sessões](/windows/desktop/TermServ/terminal-services-sessions).

Para obter mais informações sobre estações de janela, consulte os seguintes tópicos:

-   [Estação de janela e criação de área de trabalho](window-station-and-desktop-creation.md)
-   [Processar conexão com uma estação de janela](process-connection-to-a-window-station.md)
-   [Segurança de estação de janela e direitos de acesso](window-station-security-and-access-rights.md)

 

 