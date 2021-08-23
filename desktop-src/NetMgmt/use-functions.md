---
title: Usar funções
description: As funções de gerenciamento de rede examinam e gerenciam conexões (usos) entre estações de trabalho e servidores. As funções de uso são listadas a seguir.
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61019f6c6e2785f03eb4e2e9a47ed1953e14662c5664dca41465bc83d7c683d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779506"
---
# <a name="use-functions"></a>Usar funções

As funções de gerenciamento de rede examinam e gerenciam conexões (usos) entre estações de trabalho e servidores. As funções de uso são listadas a seguir.



| Função                               | Descrição                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Cria uma conexão entre um computador local e um servidor.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Encerra uma conexão com um recurso compartilhado.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Lista todas as conexões atuais entre o computador local e os recursos em servidores remotos. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Retorna informações sobre uma conexão com um recurso compartilhado.                              |



 

Essa função se aplica somente ao cliente do Bloco de Mensagens do Servidor (Estação de Trabalho do LAN Manager). A **função NetUseGetInfo** não dá suporte a compartilhamentos Sistema de Arquivos Distribuído (DFS). Para recuperar informações de conexão para um recurso compartilhado usando um provedor de rede diferente (WebDAV ou um compartilhamento DFS, por exemplo), use a [**função WNetGetConnection.**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona)

As conexões são diferenciadas das sessões: uma *sessão* é estabelecida na primeira vez que uma estação de trabalho faz uma conexão com um recurso compartilhado no servidor. Todas as conexões adicionais entre a estação de trabalho e o servidor fazem parte dessa mesma sessão até que a sessão termine. Dois tipos de conexões podem ser feitos: conexões de nome de dispositivo (que só podem ser explícitas) e conexões UNC (convenção de nomenização universal) (que podem ser explícitas ou implícitas).

*As* conexões são feitas por usuário. Uma conexão feita por um usuário é excluída quando esse usuário faz o login. Por esse motivo, as funções de uso de gerenciamento de rede são somente locais, porque uma conexão configurada por um usuário remoto não seria acessível a nenhum outro usuário, mesmo o usuário que estava conectado interativamente a esse computador.

A [**função NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) estabelece uma conexão explícita entre o computador local e um recurso compartilhado em um servidor redirecionando um nome de dispositivo local para o nome de compartilhamento de um recurso de servidor remoto \\ \\ *(servername* \\ *sharename).* Depois que uma conexão de nome de dispositivo for feita, os usuários ou aplicativos poderão usar o recurso remoto especificando o nome do dispositivo local.

As conexões UNC implícitas são feitas pela função responsável pela conexão. Para estabelecer uma conexão UNC implícita, um aplicativo passa o nome de compartilhamento de um recurso para qualquer função que aceite caminhos UNC. A função aceita o nome UNC e faz uma conexão com o nome de compartilhamento especificado. Todas as outras solicitações nessa conexão exigem o nome de compartilhamento completo.

As funções de uso estão disponíveis nos seguintes níveis de informações:

-   [**USAR \_ INFORMAÇÕES \_ 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**USAR \_ INFORMAÇÕES \_ 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**USAR \_ INFORMAÇÕES \_ 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 