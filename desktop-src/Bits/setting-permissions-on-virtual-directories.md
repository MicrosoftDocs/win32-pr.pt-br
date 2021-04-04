---
title: Definindo permissões em diretórios virtuais
description: Por motivos de segurança, Serviço de Transferência Inteligente em Segundo Plano (BITS) não carrega arquivos em um diretório virtual que tem permissões de execução e script habilitadas.
ms.assetid: cf5c8b50-066f-431e-8bdf-ed0692219b20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6753c326e926724a57e1905c3fb9fe24e28fdc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007766"
---
# <a name="setting-permissions-on-virtual-directories"></a>Definindo permissões em diretórios virtuais

Por motivos de segurança, Serviço de Transferência Inteligente em Segundo Plano (BITS) não carrega arquivos em um diretório virtual que tem permissões de execução e script habilitadas. Se você carregar um arquivo em um diretório virtual que tenha essas permissões habilitadas, o trabalho falhará com um código de erro de BG \_ E \_ execução do servidor \_ \_ habilitado.

O BITS não exige que o diretório virtual esteja habilitado para gravação, portanto, é recomendável que você desative o acesso de gravação ao diretório virtual.

O usuário autenticado (ou usuário anônimo do IIS para autenticação anônima) deve ter permissões de alteração no diretório físico para o qual o diretório virtual é mapeado; a concessão de permissões de gravação não é suficiente.

## <a name="specifying-permissions-for-notifications"></a>Especificando permissões para notificações

O esquema de autenticação especificado para o diretório virtual e a URL de notificação (consulte a propriedade [BITSServerNotificationURL](bits-iis-extension-properties.md) ) deve ser compatível. O BITS usa o esquema de autenticação especificado para o diretório virtual para acessar a URL de notificação. O trabalho de upload falhará se o BITS não puder acessar a URL de notificação devido a uma falha de autenticação.

Se o tipo de notificação (consulte a propriedade [BITSServerNotificationType](bits-iis-extension-properties.md) ) for [por referência](using-bits-notification-request-response-headers.md), o aplicativo deverá garantir que o usuário tenha acesso ao arquivo referenciado (consulte o cabeçalho [bits-Request-DataFile-Name](notification-protocol-for-server-applications.md) ). O BITS define as ACLs no arquivo referenciado para aqueles do diretório físico para o qual o diretório virtual é mapeado.

> [!Note]  
> O aplicativo notificado deve ser capaz de mapear e acessar o arquivo remoto, mesmo que a URL de notificação seja atendida por um servidor Web que esteja em um computador diferente do diretório de carregamento físico. O cabeçalho [bits-Request-DataFile-Name](notification-protocol-for-server-applications.md) sempre contém uma especificação de caminho que é relativa ao computador que hospeda o componente de extensões do bits. Um aplicativo em execução em outro computador pode precisar converter o caminho para um caminho UNC antes de acessá-lo.

 

O BITS dá suporte a muitas combinações de esquemas de autenticação. No entanto, você deve usar o seguinte esquema de autenticação para o diretório virtual e a URL de notificação de correspondência.

-   Para dar suporte a notificações de referência, o diretório virtual deve ser configurado para usar a autenticação NTLM (Negotiate) se o diretório de carregamento físico (o diretório no qual os pontos do diretório virtual) usar um esquema de autenticação diferente de anônimo. Se o diretório de carregamento físico permitir solicitações anônimas (sem autenticação), o diretório virtual deverá habilitar anônimo (sem autenticação).

    As ACLs no diretório de carregamento físico devem ser definidas de modo que o usuário autenticado possa ler arquivos no diretório para o qual a URL de notificação aponta. O BITS usa as ACLs do diretório de carregamento físico para definir as ACLs de arquivo de carregamento temporário (o cabeçalho [bits-Request-DataFile-Name](notification-protocol-for-server-applications.md) contém o caminho para o arquivo temporário).

-   Como as notificações [de valor](using-bits-notification-request-response-headers.md) não exigem que o aplicativo notificado acesse um arquivo temporário que contém o conteúdo de upload, o esquema de autenticação pode ser anônimo ou Negotiate (NTLM). O único requisito é que o usuário autenticado para o diretório virtual também deva ser autorizado a acessar a URL de notificação.

## <a name="specifying-permissions-for-remote-shares"></a>Especificando permissões para compartilhamentos remotos

Um diretório virtual pode apontar para uma unidade mapeada em um computador diferente ou um compartilhamento de rede. Se ele apontar para uma unidade de rede mapeada, as credenciais usadas para mapear a unidade deverão ter controle total sobre o compartilhamento remoto.

Se o diretório virtual apontar para um compartilhamento de rede, o BITS usará a **conexão** do diretório virtual como credenciais de usuário para acessar o compartilhamento remoto. Para acessar um compartilhamento remoto, a conta **conectar como** precisa ter privilégios, conforme descrito na documentação da função [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) . O BITS faz logon usando o lote de logon do LOGON32 \_ \_ ou \_ tipos de logon interativo de logon do LOGON32 \_ . A conta **conectar como** usuário precisa Full-Access permissões para o compartilhamento remoto; a concessão de permissões de gravação não é suficiente.

Quando o diretório de carregamento físico é mapeado para um compartilhamento de rede, a identidade do chamador que solicita a URL de notificação é o usuário **Connect** as ou o usuário autenticado do diretório físico de carregamento (disponível somente no IIS 6,0 e posterior, quando a caixa de seleção **sempre usa as credenciais do usuário autenticado ao validar o acesso ao recurso de rede** é selecionada na caixa de diálogo **conectar-se**

 

 