---
title: Pontos de conexão de serviço para serviços replicados, baseados em host e banco de dados
description: Ao publicar um serviço usando um SCP (ponto de conexão de serviço), considere como os clientes localizarão o SCP para seu serviço.
ms.assetid: 944e8ecd-f8ea-4506-992c-bbbfc82d11f3
ms.tgt_platform: multiple
keywords:
- Pontos de conexão de serviço para o AD replicado, baseado em host e serviços de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a7658cc60704dbfc37009272e5f14f997d213ea993054fa22c1c5e0c307794b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024894"
---
# <a name="service-connection-points-for-replicated-host-based-and-database-services"></a>Pontos de conexão de serviço para serviços replicados, baseados em host e banco de dados

Ao publicar um serviço usando um SCP (ponto de conexão de serviço), considere como os clientes localizarão o SCP para seu serviço. Se existirem várias instâncias do serviço, considere como os clientes distinguirão o serviço com os recursos desejados de serviços semelhantes com recursos diferentes. Se você publicar um serviço replicado, considere como um cliente escolherá uma réplica. Este tópico aborda esses problemas para vários tipos de serviços.

## <a name="replicable-services"></a>Serviços relicáveis

Para um serviço relicável, pode haver uma ou várias instâncias, ou réplicas, do serviço e os clientes não se importam com a qual réplica eles se conectam porque cada uma fornece o mesmo serviço. Active Directory Domain Services exemplos de serviços replicados: todos os controladores de domínio para determinado domínio têm dados idênticos, sujeitos à latência de replicação e fornecem serviços idênticos.

Os serviços replicados podem armazenar os SCPs e outros objetos específicos do serviço para várias réplicas em um único contêiner. O aplicativo de instalação para a primeira réplica pode criar o contêiner como um filho do contêiner Sistema do domínio local. Para obter mais informações, [consulte Publicando em um contêiner do sistema de domínio](publishing-in-a-domain-system-container.md). Verifique se o descritor de segurança do contêiner permite que os programas de instalação para réplicas subsequentes criem seus objetos no mesmo contêiner. Conceda permissões para que o administrador de instalação especifique os usuários ou grupos que podem criar ou modificar objetos no contêiner.

Uma estratégia para um serviço relicável é criar um SCP para cada réplica. Quando um cliente consulta o GUID do produto do serviço ou outra palavra-chave de identificação, ele localiza os objetos SCP para todas as réplicas e seleciona um aleatoriamente ou usando algum algoritmo de balanceamento de carga. Por exemplo, um administrador pode especificar dados de prioridade e balanceamento de carga para cada réplica, semelhantes aos campos de prioridade e peso de um registro SRV dns. O aplicativo de instalação do serviço pode armazenar esses dados no atributo **serviceBindingInformation** do SCP de cada réplica. Os clientes recuperam os dados de cada SCP e os usam para selecionar uma réplica.

Outra estratégia é criar um único SCP para todas as réplicas e definir o atributo SCP **serviceDNSName** como o nome de um registro SRV DNS. Em seguida, o aplicativo de instalação para cada réplica registra um registro SRV com esse nome. Quando um cliente identifica o SCP do serviço, o cliente recupera o nome do registro SRV e usa a função [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) para recuperar a matriz de registros SRV para as réplicas. Cada registro SRV contém o nome de um computador host e dados adicionais que o cliente pode usar para selecionar uma réplica.

## <a name="database-services"></a>Serviços de banco de dados

Instâncias diferentes de um serviço de banco de dados podem conter dados totalmente diferentes, embora sejam todos do mesmo tipo de serviço, geralmente chamados de classe de serviço. Para publicar esse tipo de serviço, o atributo **de** palavras-chave do SCP pode identificar a classe de serviço e o banco de dados específico. Um cliente de uso geral que conhece apenas o GUID da classe de serviço pode consultar todos os bancos de dados publicados por essa classe de serviço e, em seguida, apresentar uma interface do usuário para permitir que o usuário selecione um. Para um cliente projetado especificamente para o banco de dados de destino, você pode codificar o GUID do banco de dados no código do cliente.

## <a name="host-based-services"></a>Serviços baseados em host

Os serviços baseados em host são serviços que estão intimamente vinculados a um único computador host. Você pode instalar instâncias da classe de serviço em muitos computadores e cada instância fornece serviços identificados com seu computador host.

Cada instância de um serviço baseado em host deve criar seu próprio SCP no objeto de computador de seu host. Clientes que usam um GUID do produto para pesquisar o SCP de um serviço baseado em host normalmente encontram muitas instâncias da classe de serviço em toda a floresta corporativa. Os clientes podem usar o **atributo serviceDNSName** dos SCPs para encontrar o SCP para a instância de serviço no computador host desejado.

 

 