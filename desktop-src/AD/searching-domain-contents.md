---
title: Pesquisando o conteúdo do domínio
description: Antes de discutir onde associar para iniciar uma pesquisa de objetos em um domínio, é útil entender como os dados são armazenados em Active Directory Domain Services.
ms.assetid: fd0b4556-465b-4338-87cb-375450590c44
ms.tgt_platform: multiple
keywords:
- Active Directory do conteúdo do domínio
- pesquisando o conteúdo do domínio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c18cd879e950fd9c467f6674092947d430d8f87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004901"
---
# <a name="searching-domain-contents"></a>Pesquisando o conteúdo do domínio

Antes de discutir onde associar para iniciar uma pesquisa de objetos em um domínio, é útil entender como os dados são armazenados em Active Directory Domain Services.

Se você tiver uma floresta com mais de um domínio, Active Directory Domain Services não armazenará todos os dados de objeto em um único controlador de domínio — por motivos de desempenho, escalabilidade e confiabilidade. Um controlador de domínio contém todas as informações sobre apenas o domínio do qual ele é membro (ele tem uma réplica completa do domínio). Mas um controlador de domínio não contém informações completas sobre qualquer outro domínio.

Se você associar ao objeto de domínio com a procura de referência desativada, poderá pesquisar qualquer objeto nesse domínio e somente esse domínio. Para obter mais informações sobre a procura de referências, consulte [referências](referrals.md). Uma pesquisa pode recuperar qualquer propriedade e pode usar um filtro de consulta contendo qualquer propriedade.

Em uma floresta, os domínios são organizados hierarquicamente como árvores de domínio. Uma árvore de domínio pode ser apenas um domínio único ou um domínio com um ou mais domínios filho. Esses domínios filho, por sua vez, podem ter domínios filho abaixo deles. Uma árvore de domínio também é um namespace contíguo. Um namespace contíguo significa que os domínios filho são uma continuação da hierarquia de nomenclatura. Por exemplo, um domínio fabrikam.com (ou DC = Fabrikam, DC = COM) pode ter um domínio filho chamado mydivision (mydivision.fabrikam.com ou DC = mydivision, DC = Fabrikam, DC = COM), que, por sua vez, poderia ter um domínio filho chamado MyDev (mydev.mydivision.fabrikam.com ou DC = MyDev, DC = mydivision, DC = Fabrikam, DC = COM).

Se você associar a um objeto de domínio (com a procura de referência ativada) para um domínio em uma árvore de domínio, você pesquisará esse domínio e toda a hierarquia dentro dele. A pesquisa pode recuperar qualquer propriedade e pode usar um filtro de consulta contendo qualquer propriedade.

Se um controlador de domínio contiver uma réplica completa de apenas seu próprio domínio, você poderá executar uma pesquisa de subárvore em uma árvore de domínio. Um domínio mantém referências a seus domínios filho. Quando um controlador de domínio processa uma solicitação de pesquisa de subárvore em seu próprio domínio, o controlador de domínio pesquisa esse domínio e, em seguida, retorna referências a cada um de seus domínios filho para o cliente. Uma referência é a maneira como um servidor de diretório comunica que ele não contém as informações necessárias para concluir uma solicitação (como uma consulta), mas tem uma referência a um servidor que pode conter as informações necessárias. No caso de uma pesquisa de subárvore de uma árvore de domínio, uma referência é retornada para cada domínio filho direto para que a pesquisa possa continuar em um controlador de domínio em cada domínio filho. Se a procura de referência estiver ativada, a biblioteca de cliente LDAP (Wldap32.dll) usará essas referências para associar a um controlador de domínio em cada domínio filho e continuar a pesquisa. Se a busca de referência for desativada, o cliente LDAP não resolverá as referências e a pesquisa será concluída.

Uma pesquisa de subárvore em uma árvore de domínio com a caça de referência ativada pode ser demorada se houver uma conexão lenta com os controladores de domínio para os domínios filho. Se você quiser pesquisar apenas um único domínio, desative a pesquisa de referência para evitar a necessidade de Pesquisar os domínios filho desnecessariamente.

 

 




