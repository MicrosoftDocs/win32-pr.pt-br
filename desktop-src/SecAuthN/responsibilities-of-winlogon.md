---
description: Lista e explica as responsabilidades do Winlogon.
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Responsabilidades do Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6561bea11c48eb474c0ff56c5c0aa5ebfa0c22d9d6689aa55a6a208bbbc683e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919024"
---
# <a name="responsibilities-of-winlogon"></a>Responsabilidades do Winlogon

O [*Winlogon*](../secgloss/w-gly.md) tem as seguintes responsabilidades:

-   Estação de janela e proteção de área de trabalho

    O Winlogon define a proteção da estação de janela e as áreas de trabalho correspondentes para garantir que cada uma seja acessível adequadamente. Em geral, isso significa que o sistema local terá acesso total a esses objetos e que um usuário conectado interativamente terá acesso de leitura ao objeto de estação de janela e acesso completo ao objeto de área de trabalho do aplicativo.

-   Reconhecimento SAS padrão

    O Winlogon tem ganchos especiais no servidor user32 que permite que ele monitore eventos de [*sequência de atenção segura*](../secgloss/s-gly.md) (SAS) Ctrl + Alt + Del. O Winlogon torna essas informações de evento SAS disponíveis para as GINAs a serem usadas como SAS ou como parte de suas SAS. Em geral, as GINAs devem monitorar o SASs por conta própria; no entanto, qualquer [*Gina*](../secgloss/g-gly.md) que tenha a SAS padrão Ctrl + Alt + Del como uma das do SASs que ele reconhece deve usar o suporte do Winlogon fornecido para essa finalidade.

-   Expedição de rotina SAS

    Quando o Winlogon encontra um evento SAS ou quando uma SAS é entregue ao Winlogon pela GINA, o Winlogon define o estado de acordo, muda para a área de trabalho do Winlogon e chama uma das funções de processamento de SAS da GINA.

-   Carregamento de perfil do usuário

    Quando os usuários fazem logon, seus perfis de usuário são carregados no registro. Dessa forma, os processos do usuário podem usar a chave do registro especial HKEY \_ Current \_ User. O Winlogon faz isso automaticamente após um logon bem-sucedido, mas antes da ativação do Shell para o usuário conectado recentemente.

-   Atribuição de segurança ao shell do usuário

    Quando um usuário faz logon, a GINA é responsável por criar um ou mais processos iniciais para esse usuário. O Winlogon fornece uma função de suporte para a GINA aplicar a segurança do usuário conectado recentemente a esses processos. no entanto, a maneira preferida de fazer isso é que a GINA chame a função de Windows [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)e deixe que o sistema forneça o serviço.

-   Controle de proteção de tela

    O Winlogon monitora a atividade de teclado e mouse para determinar quando ativar as proteções de tela. Depois que a proteção de tela é ativada, o Winlogon continua a monitorar a atividade de teclado e mouse para determinar quando encerrar a proteção de tela. Se a proteção de tela estiver marcada como segura, o Winlogon tratará a estação de trabalho como bloqueada. Quando há atividade de mouse ou de teclado, o Winlogon invoca a função [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) da Gina e o comportamento de estação de trabalho bloqueado continua. Se a proteção de tela não for segura, qualquer atividade de teclado ou mouse terminará a proteção de tela sem notificação para a GINA.

-   Suporte a vários provedores de rede

    várias redes instaladas em um sistema Windows podem ser incluídas no processo de autenticação e em operações de atualização de senha. Essa inclusão permite que redes adicionais coletem informações de identificação e autenticação de uma só vez durante o logon normal, usando a área de trabalho segura do Winlogon. Alguns dos parâmetros necessários nos serviços do Winlogon disponíveis para as GINAs oferecem suporte explícito a esses provedores de rede adicionais.

 

 
