---
title: Estações de Janela
description: Uma estação de janela contém uma área de transferência, uma tabela atom e um ou mais objetos da área de trabalho. Cada objeto de estação de janela é um objeto securável. Quando uma estação de janela é criada, ela é associada ao processo de chamada e atribuída à sessão atual.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- objetos da estação de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d55e43a0db21b23a6704949f0d72a184c9034f625689b800814ac8a93891b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199687"
---
# <a name="window-stations"></a>Estações de Janela

Uma *estação de janela* contém uma área de transferência, uma tabela atom e um ou mais objetos da área [de](desktops.md) trabalho. Cada objeto de estação de janela é um objeto securável. Quando uma estação de janela é criada, ela é associada ao processo de chamada e atribuída à sessão atual.

A *estação de janela interativa* é a única estação de janela que pode exibir uma interface do usuário ou receber entrada do usuário. Ele é atribuído à sessão de logon do usuário interativo e contém o teclado, o mouse e o dispositivo de exibição. Ele sempre é chamado de "WinSta0". Todas as outras estações de janela são não interativas, o que significa que elas não podem exibir uma interface do usuário ou receber entrada do usuário.

Quando um usuário faz logon em um computador usando Serviços de Área de Trabalho Remota, uma sessão é iniciada para o usuário. Cada sessão é associada à sua própria estação de janela interativa chamada "WinSta0". Para obter mais informações, [consulte Área de Trabalho Remota sessões](/windows/desktop/TermServ/terminal-services-sessions).

Para obter mais informações sobre estações de janela, consulte os seguintes tópicos:

-   [Estação de Janelas e Criação da Área de Trabalho](window-station-and-desktop-creation.md)
-   [Processar conexão com uma estação de janela](process-connection-to-a-window-station.md)
-   [Segurança e direitos de acesso da estação de janela](window-station-security-and-access-rights.md)

 

 