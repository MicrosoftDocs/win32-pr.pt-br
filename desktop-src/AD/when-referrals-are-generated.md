---
title: Quando as indicações são geradas
description: Uma indicação é a maneira como um servidor de diretório comunica que ele não contém os dados necessários para concluir uma consulta, mas tem uma referência a um servidor que pode conter os dados necessários.
ms.assetid: 2c11a52a-26e2-4a50-a0a3-5463a0852b27
ms.tgt_platform: multiple
keywords:
- geração de indicações active directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1eb05d1495e1f6884d6ce6123356ed29235da421839042909fc05aaa4d9d67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182159"
---
# <a name="when-referrals-are-generated"></a>Quando as indicações são geradas

Uma indicação é a maneira como um servidor de diretório comunica que ele não contém os dados necessários para concluir uma consulta, mas tem uma referência a um servidor que pode conter os dados necessários. Esteja ciente de que as indicações não são geradas apenas por solicitações de consulta.

As seguintes operações podem resultar em uma ou mais indicações:

-   Associação a um servidor que não contém o objeto especificado pelo nome diferenciado solicitado, mas tem dados sobre um servidor ou domínio que pode conter esse objeto. Para ADSI, isso pode ocorrer se o aplicativo chamar [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) ou [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) para se vincular a um objeto que existe em outro domínio na floresta (indicação interna) ou um contexto de nomen por completo separado da floresta (indicação externa). Para a API LDAP, isso pode ocorrer ao executar operações de adicionar, modificar, excluir ou pesquisar que especificam um objeto que existe em outro domínio na floresta (indicação interna) ou um contexto de nomen por completo separado da floresta (indicação externa).

    Se a resolução de nomes não encontrar um objeto localmente e não houver objetos **crossRef** para essa parte do namespace, o controlador de domínio tentará construir uma indicação externa com base nos componentes de domínio do nome diferenciado. Por exemplo, se uma pesquisa foi baseada em "CN=a,CN=b,DC=c,DC=d,DC=e", o controlador de domínio construirá uma indicação para o servidor LDAP no endereço DNS "c.d.e".

    Todos Windows controladores de domínio 2000 (que só suportam DC= nomen vista para os componentes superiores) reconhecem uns aos outros e nenhuma referência cruzada externa é necessária para um cliente se vincular de uma floresta a outra. Se outros servidores de diretório não Windows 2000, como um servidor Netscape, estiver usando DC= nomenu e tiver um RR SRV apropriado registrado no DNS, ele também obterá a vantagem das indicações automáticas. Caso não seja, um **objeto crossRef** externo deve ser adicionado manualmente.

-   Executar uma pesquisa de subárvore em um domínio que contém domínios subordinados na floresta ou domínios externos subordinados, esquema ou contêineres de configuração. Uma indicação para o domínio subordinado, domínio externo, esquema ou contêiner de configuração será criada. Se a indicação for habilitada, a indicação será transparente para o chamador.

 

 