---
title: Referências (AD DS)
description: Active Directory Domain Services manter dados de referência em objetos crossRef armazenados no contêiner de partições (crossRefContainer) no contêiner de configuração.
ms.assetid: e4d6cc8a-9c2c-4e0f-acca-e9ecdd5e879b
ms.tgt_platform: multiple
keywords:
- ANÚNCIOS de referências
- Active Directory, referências
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63c87fb0248d85ab20191296f9659eb58e460f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105750381"
---
# <a name="referrals-ad-ds"></a>Referências (AD DS)

Active Directory Domain Services manter dados de referência em objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) armazenados no contêiner de partições ([**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer)) no contêiner de configuração. No tópico [decidindo onde Pesquisar](where-to-search.md) , as referências são discutidas no contexto de um domínio em uma árvore de domínio e a geração de referências a domínios subordinados em uma pesquisa de subárvore.

Active Directory Domain Services criar e manter objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) para todos os domínios na floresta. Além disso, há objetos **crossRef** para os contêineres de configuração e esquema. Esses objetos **crossRef** são usados para gerar referências em resposta a consultas que solicitam dados sobre objetos que existem na floresta, mas não estão contidos no servidor de diretório que manipula a solicitação. Elas são chamadas de *referências cruzadas internas*, pois se referem a domínios, esquemas e contêineres de configuração dentro da floresta.

Se a busca de referência não estiver habilitada e uma pesquisa de subárvore for executada, a pesquisa retornará todos os objetos dentro do domínio especificado que atendem aos critérios de pesquisa. A pesquisa também retornará referências a quaisquer domínios subordinados que sejam descendentes diretos do domínio do servidor de diretório. O cliente deve resolver as referências ligando-se ao caminho especificado pela referência e enviando outra consulta.

Se a procura de referência estiver ativada e uma pesquisa de subárvore for executada, a API LDAP subjacente tentará automaticamente se associar a quaisquer referências e adicionará os resultados da pesquisa ao conjunto de resultados. Na maioria dos casos, a caça de referência será transparente para o chamador. Se a referência for para um objeto em um domínio ou floresta diferente, a API LDAP subjacente tentará usar as credenciais atuais para associar ao destino da referência. Se isso for bem-sucedido, a caça de referência será transparente. Se isso não for bem-sucedido, a referência e um código de erro de referência serão retornados.

Para obter mais informações sobre como definir a preferência de pesquisa de busca de referência, consulte [especificando outras opções de pesquisa](specifying-other-search-options.md).

Além do [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot) (nome DNS do domínio) e das propriedades do [**NCName**](/windows/desktop/ADSchema/a-ncname) (nome distinto para o domínio), o objeto [**CROSSREF**](/windows/desktop/ADSchema/c-crossref) também contém o **NetBiosName** (nome NetBIOS do domínio) e **trustParent** (nome distinto para o objeto **crossRef** que representa as propriedades do domínio pai direto do domínio).

Active Directory Domain Services também pode ter *referências cruzadas externas* que se referem a objetos fora da floresta. As referências cruzadas externas devem ser adicionadas explicitamente por um administrador. Lembre-se de que o servidor de destino da referência cruzada externa deve ter uma raiz DNS; ou seja, ele deve aderir ao RFC 2247.

Uma referência cruzada externa se refere a um objeto em qualquer outra floresta, desde que o nome seja exclusivo na floresta de destino. Por exemplo, os aplicativos cliente LDAP usados por sua empresa podem enviar operações para seus servidores de diretório para Fabrikam.com. Você cria um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) para fabrikam.com. Agora, em vez de retornar um erro de objeto não encontrado, os servidores de diretório podem retornar uma referência a um objeto no domínio Fabrikam.com e os clientes podem perseguir a referência. Por exemplo, se você tiver um objeto com o seguinte nome distinto:


```C++
CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



Você pode adicionar uma referência cruzada externa para um objeto com o nome "ChildOfSomeObject".


```C++
CN=ChildOfSomeObject,CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



Uma pesquisa de subárvore que contém "SomeObject" também retornará uma referência a "ChildOfSomeObject". Lembre-se de que deve haver um servidor LDAP no endereço especificado pela referência (uma das propriedades no objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) ) e que esse servidor LDAP deve fornecer o namespace que é identificado por "ChildOfSomeObject".

Como os objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) são armazenados no contêiner de configuração, cada DC (controlador de domínio) tem uma cópia de todos os objetos **crossRef** . Portanto, cada DC contém dados sobre cada domínio na floresta, bem como suas relações superiores/subordinadas. Isso permite que cada DC gere referências a qualquer domínio na floresta e as referências para o domínio subordinado, o esquema ou os contêineres de configuração não explorados em uma pesquisa de subárvore.

Para obter mais informações sobre referências, consulte:

-   [Quando as referências são geradas](when-referrals-are-generated.md)
-   [Criando uma referência externa](creating-an-external-referral.md)

Para obter mais informações e um exemplo de código que mostra como obter o nome distinto do contêiner partições, consulte [código de exemplo para localizar o contêiner partições](example-code-for-locating-the-partitions-container.md).

 

 