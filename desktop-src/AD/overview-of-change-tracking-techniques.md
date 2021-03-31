---
title: Visão geral das técnicas de Controle de Alterações
description: Há várias maneiras pelas quais os mecanismos de controle de alterações podem variar o escopo para controlar alterações um aplicativo pode controlar alterações em um único atributo de um único objeto, em todos os objetos de um domínio e assim por diante.
ms.assetid: 7359e851-61b7-420d-beb0-f7f33f79b007
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91fce20dc5e9fe8fe98937bb13885be577185e04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004906"
---
# <a name="overview-of-change-tracking-techniques"></a>Visão geral das técnicas de Controle de Alterações

Há várias maneiras pelas quais os mecanismos de controle de alterações podem diferir:

-   Escopo para controlar alterações: um aplicativo pode controlar alterações em um único atributo de um único objeto, em todos os objetos em um domínio e assim por diante. Se o mecanismo corresponder aos requisitos do aplicativo, o aplicativo receberá um mínimo de dados irrelevantes e, portanto, isso melhora o desempenho.
-   Cronograma: um aplicativo é notificado sobre cada alteração conforme ele acontece ou pode ser notificado do efeito líquido das alterações em um período de minutos ou horas.

    O processamento de dados menos oportunos pode ser mais eficiente, pois várias alterações podem ser recolhidas em um. Por exemplo, se um atributo for alterado três vezes em um intervalo de uma hora, um aplicativo notificado sobre as alterações acumuladas em uma hora será notificado de apenas uma alteração de atributo, e não de três.

    Ao pensar sobre a linha do tempo, considere o efeito da latência de replicação. Uma atualização que se origina em um controlador de domínio não é replicada instantaneamente para outro controlador de domínio. Exigir uma linha de tempo de controle de alterações muito melhor do que a latência de replicação esperada geralmente não oferece nenhum benefício real para o aplicativo.

-   Sondagem versus notificação: com sondagem, um aplicativo faz periodicamente uma solicitação a um controlador de domínio para receber dados de controle de alterações. Com a notificação, o controlador de domínio envia as alterações para o aplicativo somente quando ocorrerem alterações.

    A sobrecarga de sondagem é óbvia: o aplicativo pode solicitar dados de controle de alterações quando nada significativo tiver ocorrido. A sobrecarga da notificação é mais sutil. O servidor deve manter dados sobre solicitações de notificação e deve consultar esses dados para decidir se deseja ou não enviar uma notificação. Isso pode adicionar sobrecarga às solicitações de atualização normais.

-   Expressar o conhecimento do aplicativo: persistente versus temporário: cada mecanismo de controle de alterações deve incluir algum método para o servidor que contém os dados rastreados para entender o estado de conhecimento do aplicativo, para que a ideia de "alteração" esteja bem definida. Por exemplo, o estado de conhecimento do aplicativo pode ser expresso como "atualizado com todas as alterações ocorridas no DC d antes do tempo t". Um mecanismo com base nessa forma de expressar o estado de conhecimento de um aplicativo forneceria uma maneira eficiente para o aplicativo obter alterações que ocorreram depois do tempo especificado.

    Se a expressão do conhecimento do aplicativo puder ser persistida, ou seja, armazenada em recuperação, como em um arquivo ou banco de dados, a reinicialização do aplicativo será menos intensiva de recursos do que se não puder. No exemplo acima, a expressão do conhecimento do aplicativo pode ser persistida gravando o DC d e a hora t. Alguns mecanismos de notificação de alteração não permitem que esses dados sejam persistidos. O servidor e o aplicativo devem sincronizar com algum outro mecanismo quando o aplicativo é iniciado. Isso é intensivo de recursos se vários objetos estiverem envolvidos e puder envolver programação complexa.

Use as seguintes técnicas para controlar as alterações no Active Directory Domain Services:

-   Use o controle de notificação de alteração para iniciar uma pesquisa assíncrona persistente para alterações que correspondam a um filtro especificado. Para obter mais informações, consulte [Change Notifications in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md).
-   Use uma pesquisa de sincronização de diretório (DirSync) para recuperar as alterações ocorridas desde a pesquisa do DirSync anterior. Para obter mais informações, consulte [sondando alterações usando o controle DirSync](polling-for-changes-using-the-dirsync-control.md).
-   Use o atributo USNChanged para pesquisar objetos que foram alterados desde a pesquisa anterior. Para obter mais informações, consulte [sondando alterações usando USNChanged](polling-for-changes-using-usnchanged.md).

O controle de notificação de alteração foi projetado para aplicativos ou serviços que exigem notificação de aviso razoável de alterações infrequentes. Um exemplo é um serviço ou programa que armazena dados de configuração no servidor Active Directory e deve ser notificado imediatamente quando ocorre uma alteração. Lembre-se de que há limitações do controle de notificação.

-   A solicitação de notificações depende da latência de replicação e do local em que a alteração ocorreu. Você pode ser notificado imediatamente quando uma alteração Replica na réplica que você está monitorando, mas a alteração pode ter se originado muito mais cedo em alguma outra réplica.
-   O controle é restrito a monitorar um único objeto ou os filhos imediatos de um contêiner. Os aplicativos que devem monitorar vários contêineres ou objetos não relacionados podem registrar até cinco solicitações de notificação.
-   Se muitos clientes estiverem ouvindo alterações que ocorrem com frequência, ele afetará o desempenho do servidor. Em geral, os aplicativos devem limitar o uso desse controle por motivos de desempenho no servidor. Se você não precisar saber sobre as alterações imediatamente, pode ser melhor sondar periodicamente as alterações em vez de usar a notificação de alteração.

As técnicas de pesquisa DirSync e USNChanged são projetadas para aplicativos que mantêm a consistência entre os dados no servidor de Active Directory e os dados correspondentes em algum outro armazenamento. Essas técnicas são usadas por aplicativos que sondam periodicamente as alterações. A técnica DirSync baseia-se em um controle de servidor LDAP que você pode usar por meio de APIs ADSI ou LDAP. As desvantagens do controle DirSync são que ele só pode ser usado por uma conta altamente privilegiada, como um administrador de domínio. A seguir está uma lista de limitações do controle DirSync:

-   O controle DirSync só pode ser usado por uma conta altamente privilegiada, como um administrador de domínio.
-   O controle DirSync só pode monitorar um contexto de nomenclatura inteiro. Não é possível limitar o escopo de uma pesquisa DirSync para monitorar apenas uma subárvore, um contêiner ou um objeto específico em um contexto de nomenclatura.

A técnica USNChanged não tem essas limitações, embora seja um pouco mais complicada de usar do que o DirSync.

 

 




