---
title: Quando as referências são geradas
description: Uma referência é a maneira como um servidor de diretório comunica que ele não contém os dados necessários para concluir uma consulta, mas tem uma referência a um servidor que pode conter os dados necessários.
ms.assetid: 2c11a52a-26e2-4a50-a0a3-5463a0852b27
ms.tgt_platform: multiple
keywords:
- Active Directory de geração de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e47c1e172f3eaed34dad452aa46847980cd66f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823625"
---
# <a name="when-referrals-are-generated"></a>Quando as referências são geradas

Uma referência é a maneira como um servidor de diretório comunica que ele não contém os dados necessários para concluir uma consulta, mas tem uma referência a um servidor que pode conter os dados necessários. Lembre-se de que as referências não são geradas apenas por solicitações de consulta.

As seguintes operações podem resultar em uma ou mais referências:

-   Associação a um servidor que não contém o objeto especificado pelo nome distinto solicitado, mas tem dados sobre um servidor ou domínio que pode conter esse objeto. Para ADSI, isso pode ocorrer se o aplicativo chamar [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) ou [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) para associar a um objeto que existe em outro domínio na floresta (referência interna) ou a um contexto de nomenclatura que é completamente separado da floresta (referência externa). Para a API LDAP, isso pode ocorrer ao executar operações de adicionar, modificar, excluir ou Pesquisar que especificam um objeto que existe em outro domínio na floresta (referência interna) ou um contexto de nomenclatura que é completamente separado da floresta (referência externa).

    Se a resolução de nomes não localizar um objeto localmente e não houver objetos **crossRef** para essa parte do namespace, o controlador de domínio tentará construir uma referência externa com base nos componentes de domínio do nome distinto. Por exemplo, se uma pesquisa fosse baseada em "CN = a, CN = b, DC = c, DC = d, DC = e", o controlador de domínio criará uma referência ao servidor LDAP no endereço DNS "c. d. e".

    Todos os controladores de domínio do Windows 2000 (que dão suporte apenas a DC = nomenclatura para os componentes superiores) reconhecem um ao outro, e nenhuma referência cruzada externa é necessária para que um cliente seja associado de uma floresta para outra. Se outros servidores de diretório não Windows 2000, como um servidor Netscape, estiverem usando DC = Naming e tiverem um RR SRV apropriado registrado no DNS, ele também obterá a vantagem das referências automáticas. Caso contrário, um objeto **crossRef** externo deverá ser adicionado manualmente.

-   Executar uma pesquisa de subárvore em um domínio que contém domínios subordinados na floresta ou em domínios externos subordinados, esquema ou contêineres de configuração. Uma referência ao domínio subordinado, ao domínio externo, ao esquema ou ao contêiner de configuração será criada. Se a caça de referência estiver habilitada, a referência será transparente para o chamador.

 

 