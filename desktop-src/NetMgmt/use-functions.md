---
title: Usar funções
description: As funções de uso de gerenciamento de rede examinam e gerenciam conexões (usos) entre estações de trabalho e servidores. As funções de uso são listadas a seguir.
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2660b911fd87c39b9db10b0dbfea0e47c484c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823940"
---
# <a name="use-functions"></a>Usar funções

As funções de uso de gerenciamento de rede examinam e gerenciam conexões (usos) entre estações de trabalho e servidores. As funções de uso são listadas a seguir.



| Função                               | Descrição                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Cria uma conexão entre um computador local e um servidor.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Finaliza uma conexão com um recurso compartilhado.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Lista todas as conexões atuais entre o computador local e os recursos em servidores remotos. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Retorna informações sobre uma conexão a um recurso compartilhado.                              |



 

Essas funções se aplicam somente ao cliente do protocolo de estação de mensagens do servidor (LAN Manager). A função **NetUseGetInfo** não oferece suporte a compartilhamentos de sistema de arquivos distribuído (DFS). Para recuperar informações de conexão para um recurso compartilhado usando um provedor de rede diferente (WebDAV ou um compartilhamento DFS, por exemplo), use a função [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) .

As conexões são diferenciadas de sessões: uma *sessão* é estabelecida na primeira vez que uma estação de trabalho faz uma conexão com um recurso compartilhado no servidor. Todas as conexões adicionais entre a estação de trabalho e o servidor fazem parte dessa mesma sessão até que a sessão termine. Dois tipos de conexões podem ser feitas: conexões de nome de dispositivo (que só podem ser explícitas) e conexões UNC (Convenção de nomenclatura universal) (que podem ser explícitas ou implícitas).

*As conexões* são feitas em uma base por usuário. Uma conexão feita por um usuário é excluída quando o usuário faz logoff. Por esse motivo, as funções de uso de gerenciamento de rede são somente locais, porque uma conexão configurada por um usuário remoto não estaria acessível a nenhum outro usuário, até mesmo o que estava conectado interativamente ao computador.

A função [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) estabelece uma conexão explícita entre o computador local e um recurso compartilhado em um servidor redirecionando um nome de dispositivo local para o nome do compartilhamento de um recurso de servidor remoto ( \\ \\ *nomedoservidor* \\ *ShareName*). Depois que uma conexão de nome de dispositivo é feita, os usuários ou aplicativos podem usar o recurso remoto especificando o nome do dispositivo local.

As conexões UNC implícitas são feitas pela função responsável pela conexão. Para estabelecer uma conexão UNC implícita, um aplicativo passa o nome do compartilhamento de um recurso para qualquer função que aceite caminhos UNC. A função aceita o nome UNC e estabelece uma conexão com o nome de compartilhamento especificado. Todas as solicitações adicionais nesta conexão exigem o nome completo do compartilhamento.

As funções de uso estão disponíveis nos seguintes níveis de informações:

-   [**USAR \_ informações \_ 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**USAR \_ informações \_ 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**USAR \_ informações \_ 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 