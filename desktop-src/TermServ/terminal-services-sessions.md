---
title: Sessões de Área de Trabalho Remota
description: Como cada logon em um cliente de Conexão de Área de Trabalho Remota (RDC) recebe uma ID de sessão separada, a experiência do usuário é semelhante a ser conectada a vários computadores ao mesmo tempo; por exemplo, um computador do escritório e um computador doméstico.
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb99f9745e382bdff1099eabae9a8e8ef0b8333
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105756802"
---
# <a name="remote-desktop-sessions"></a>Sessões de Área de Trabalho Remota

Quando um usuário faz logon em um computador com Serviços de Área de Trabalho Remota habilitado, uma sessão é iniciada para o usuário. Cada sessão é identificada por uma ID de sessão exclusiva. Como cada logon em um cliente de Conexão de Área de Trabalho Remota (RDC) recebe uma ID de sessão separada, a experiência do usuário é semelhante a ser conectada a vários computadores ao mesmo tempo; por exemplo, um computador do escritório e um computador doméstico.

Cada sessão de área de trabalho remota é associada a uma estação de janela interativa. O único nome de estação de janela com suporte para uma estação de janela interativa é "WinSta0"; Portanto, cada sessão é associada à sua própria estação de janela "WinSta0". Há três áreas de trabalho padrão para cada estação de janela: a área de trabalho do Winlogon, a área de trabalho de proteção de tela e a área de trabalho interativa.

O usuário associado à estação de janela interativa para uma sessão é conhecido como *usuário interativo*. Em um cliente Conexão de Área de Trabalho Remota (RDC), pode haver vários usuários interativos além do usuário interativo no console do Serviços de Área de Trabalho Remota. Para recuperar o identificador da sessão atualmente anexada ao console, use a função [**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid) .

Quando um usuário faz logoff de um cliente de Conexão de Área de Trabalho Remota (RDC), a sessão que o cliente tem no servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) (anteriormente conhecido como um servidor de terminal) é excluída e as estações de janela e áreas de trabalho associadas a essa sessão são removidas. No entanto, como a sessão de console do Serviços de Área de Trabalho Remota nunca é excluída, as estações de janela associadas à sessão do console não são excluídas. Isso afeta a forma como os aplicativos se comportam em um ambiente de Serviços de Área de Trabalho Remota quando são configurados para execução no contexto de segurança do usuário interativo, também conhecido como o modo de ativação de objeto "RunAs Interactive User".

Para obter mais informações sobre como iniciar um processo de servidor local em uma sessão especificada, consulte [ativação de sessão para sessão com um moniker de sessão](session-to-session-activation-with-a-session-moniker.md) e [usando um moniker de sessão](using-a-session-moniker.md). Para obter mais informações sobre contextos de segurança, consulte [o contexto de segurança do cliente](/windows/desktop/SecAuthZ/the-client-security-context).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessões filho](child-sessions.md)
</dt> </dl>

 

 