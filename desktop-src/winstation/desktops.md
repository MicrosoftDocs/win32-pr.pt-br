---
title: Desktops
description: Uma área de trabalho tem uma superfície de exibição lógica e contém objetos de interface do usuário, como Windows, menus e ganchos; Ele pode ser usado para criar e gerenciar o Windows.
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- objetos da área de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b763c05c3d45c701da0bdd606fa906dec3f8af07ce72d256b402e7df5d9319b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587346"
---
# <a name="desktops"></a>Desktops

Uma *área de trabalho* tem uma superfície de exibição lógica e contém objetos de interface do usuário, como Windows, menus e ganchos; Ele pode ser usado para criar e gerenciar o Windows. Cada objeto da área de trabalho é um objeto protegível. Quando uma área de trabalho é criada, ela é associada à [estação de janela](window-stations.md) atual do processo de chamada e atribuída ao thread de chamada.

As mensagens de janela podem ser enviadas somente entre processos que estão na mesma área de trabalho. Além disso, o procedimento de gancho de um processo em execução em uma área de trabalho específica só pode receber mensagens destinadas ao Windows criado na mesma área de trabalho.

As áreas de trabalho associadas à estação de janela interativa, Winsta0, podem ser feitas para exibir uma interface do usuário e receber a entrada do usuário, mas apenas uma dessas áreas de trabalho por vez está ativa. Esse desktop ativo, também conhecido como a *área de trabalho de entrada*, é aquele que está visível no momento para o usuário e que recebe a entrada do usuário. Os aplicativos podem usar a função [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) para obter um identificador para a área de trabalho de entrada. Os aplicativos que têm o acesso necessário podem usar a função [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) para especificar uma área de trabalho de entrada diferente.

Por padrão, há três áreas de trabalho na estação de janela interativa: padrão, proteção de tela e Winlogon.

A área de trabalho padrão é criada quando o Winlogon inicia o processo inicial como o usuário conectado. Nesse ponto, a área de trabalho padrão torna-se ativa e é usada para interagir com o usuário.

Sempre que uma proteção de tela segura é ativada, o sistema alterna automaticamente para a área de trabalho de proteção de segurança, que protege os processos na área de trabalho padrão de usuários não autorizados. As proteções de tela não seguras são executadas no \\ padrão Winsta0.

A área de trabalho do Winlogon está ativa enquanto um usuário faz logon. O sistema muda para a área de trabalho padrão quando o Shell indica que está pronto para exibir algo ou após trinta segundos, o que ocorrer primeiro. Durante a sessão do usuário, o sistema alterna para a área de trabalho do Winlogon quando o usuário pressiona a sequência de teclas CTRL + ALT + DEL ou quando a caixa de diálogo controle de conta de usuário (UAC) está aberta.

**Windows Server 2003 e Windows XP/2000:** Não há suporte para a caixa de diálogo UAC.

O descritor de segurança da área de trabalho do Winlogon permite o acesso a um conjunto muito restrito de contas, incluindo a [conta LocalSystem](/windows/desktop/Services/localsystem-account). Os aplicativos geralmente não carregam nenhum dos SIDs de uma das contas em seus tokens e, portanto, não podem acessar a área de trabalho do Winlogon ou alternar para uma área de trabalho diferente enquanto a área de trabalho do Winlogon está ativa.

Para obter mais informações, consulte estes tópicos:

-   [Estação de janela e criação de área de trabalho](window-station-and-desktop-creation.md)
-   [Conexão de thread com uma área de trabalho](thread-connection-to-a-desktop.md)
-   [Segurança de desktop e direitos de acesso](desktop-security-and-access-rights.md)

 

 