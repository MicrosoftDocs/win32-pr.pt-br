---
description: Em sistemas operacionais mais antigos, era necessário fazer logoff de um usuário para que outro usuário pudesse fazer logon. A partir do Windows XP, um usuário não precisa fazer logoff para permitir que outro usuário faça logon.
ms.assetid: 72f99d32-184f-4f0b-bec1-6068c6e32f88
title: Troca rápida de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d79f16ef8a1ea8c97bfb61d34dfa727f3d0cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104989004"
---
# <a name="fast-user-switching"></a>Troca rápida de usuário

Quando um usuário faz logon em um computador, o sistema carrega seu perfil. Como cada usuário tem uma conta de usuário exclusiva, isso permite que vários usuários compartilhem um computador. Quando um usuário faz logon, as configurações da área de trabalho, os arquivos, os favoritos e o histórico que eles veem são seus. Eles não podem ser acessados por outros usuários. Quando esse usuário fizer logoff, seu perfil será preservado na próxima vez em que fizerem logon. Em sistemas operacionais mais antigos, era necessário fazer logoff de um usuário para que outro usuário pudesse fazer logon. A partir do Windows XP, um usuário não precisa fazer logoff para permitir que outro usuário faça logon. Em vez disso, é possível que vários usuários façam logon e alternem rapidamente entre suas contas abertas. Esse recurso é chamado de *troca rápida de usuário*. Alternar para outra conta não altera o estado dos aplicativos que um usuário está executando no momento. Suponha, por exemplo, que um usuário permita que outro usuário alterne para sua conta enquanto o primeiro usuário estiver conectado. Quando o primeiro usuário muda de volta para sua conta, seus aplicativos estão em execução e suas conexões de rede são preservadas. Portanto, parece que ambos os usuários estão usando o computador simultaneamente.

Se seus aplicativos estiverem em conformidade com os requisitos de logotipo do Windows 2000, eles deverão trabalhar com troca rápida de usuário no Windows XP e sistemas operacionais posteriores. No entanto, é importante manter esse cenário em mente ao desenvolver um aplicativo para que ele se comporta como os usuários esperam. Use as seguintes diretrizes ao escrever seus aplicativos:

-   Implemente a verdadeira separação de perfil. O sistema fornece uma infraestrutura subjacente que dá suporte à separação de dados do usuário, configurações do usuário e configurações do computador. Por exemplo, use a pasta **documentos** do usuário para armazenar dados criados pelo usuário. Para localizar um diretório para dados específicos do aplicativo, use o sistema de [pastas conhecido](known-folders.md) com [**FolderId \_ RoamingAppData**](knownfolderid.md)) ou, para sistemas operacionais mais antigos, o sistema de [**CSIDL**](csidl.md) com [**CSIDL \_ AppData**](csidl.md)). Use **FolderId \_ LocalAppData** ou **CSIDL \_ local \_ AppData** para dados que não devem estar disponíveis para o usuário em outros computadores, como arquivos temporários.
-   Registre-se para notificação de um comutador de usuário. Normalmente, um aplicativo não precisa ser notificado quando ocorre a mudança. No entanto, se seu aplicativo precisar ser notificado sobre uma alteração de sessão, ele poderá se registrar para receber uma mensagem de [**\_ \_ alteração do WM WTSSESSION**](../termserv/wm-wtssession-change.md) .
-   Lembre-se de outras instâncias do seu aplicativo. Por exemplo, há ocasiões em que um aplicativo deve baixar uma atualização da Internet. A atualização poderá falhar se outro usuário estiver executando simultaneamente uma instância do aplicativo em outra sessão. Mesmo que a atualização tenha sucesso, a atualização pode fazer com que outras instâncias em execução do aplicativo se comportem de forma imprevisível. Portanto, é melhor executar uma atualização dinâmica somente se nenhuma outra instância do aplicativo estiver em execução. Antes de baixar uma atualização de aplicativo, pode ser apropriado implementar um método que sinalize todas as instâncias em execução do aplicativo para salvar dados e sair corretamente.

 

 
