---
title: Pontos de conexão de serviço para serviços replicados, baseados em host e de banco de dados
description: Quando você publica um serviço usando um SCP (ponto de conexão de serviço), considere como os clientes irão localizar o SCP para seu serviço.
ms.assetid: 944e8ecd-f8ea-4506-992c-bbbfc82d11f3
ms.tgt_platform: multiple
keywords:
- Pontos de conexão de serviço para AD replicados, baseados em host e de serviços de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b69491dd84a9367f8fd05e9d23ca771551dfbb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007289"
---
# <a name="service-connection-points-for-replicated-host-based-and-database-services"></a>Pontos de conexão de serviço para serviços replicados, baseados em host e de banco de dados

Quando você publica um serviço usando um SCP (ponto de conexão de serviço), considere como os clientes irão localizar o SCP para seu serviço. Se houver várias instâncias do serviço, considere como os clientes distinguirão o serviço com os recursos desejados de serviços semelhantes com diferentes recursos. Se você publicar um serviço replicado, considere como um cliente escolherá uma réplica. Este tópico discute esses problemas para vários tipos de serviços.

## <a name="replicable-services"></a>Serviços replicáveis

Para um serviço replicável pode haver uma ou mais instâncias, ou réplicas, do serviço, e os clientes não se preocupam com a qual réplica eles se conectam porque cada uma fornece o mesmo serviço. Active Directory Domain Services são exemplos de serviços replicados: todos os controladores de domínio para um determinado domínio contêm dados idênticos, sujeitos à latência de replicação e fornecem serviços idênticos.

Os serviços replicáveis podem armazenar o SCPs e outros objetos específicos de serviço para várias réplicas em um único contêiner. O aplicativo de instalação para a primeira réplica pode criar o contêiner como um filho do contêiner do sistema do domínio local. Para obter mais informações, consulte [publicando em um contêiner do sistema de domínio](publishing-in-a-domain-system-container.md). Verifique se o descritor de segurança do seu contêiner permite que os programas de instalação para réplicas subsequentes criem seus objetos no mesmo contêiner. Conceda permissões para que o administrador de instalação especifique os usuários ou grupos que podem criar ou modificar objetos no contêiner.

Uma estratégia para um serviço replicável é criar um SCP para cada réplica. Quando um cliente consulta o GUID do produto do serviço ou outra palavra-chave de identificação, ele localiza os objetos SCP para todas as réplicas e seleciona uma aleatoriamente ou usando algum algoritmo de balanceamento de carga. Por exemplo, um administrador poderia especificar a prioridade e os dados de balanceamento de carga para cada réplica, semelhante aos campos de prioridade e peso de um registro SRV do DNS. O aplicativo de instalação do serviço pode armazenar esses dados no atributo **ServiceBindingInformation** do SCP de cada réplica. Os clientes recuperam os dados de cada SCP e usam-os para selecionar uma réplica.

Outra estratégia é criar um único SCP para todas as réplicas e definir o atributo SCP **serviceDNSName** como o nome de um registro SRV do DNS. Em seguida, o aplicativo de instalação para cada réplica registra um registro SRV com esse nome. Quando um cliente identifica o SCP solitário do serviço, o cliente recupera o nome do registro SRV e usa a função [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) para recuperar a matriz de registros SRV para as réplicas. Cada registro SRV contém o nome de um computador host e dados adicionais que o cliente pode usar para selecionar uma réplica.

## <a name="database-services"></a>Serviços de banco de dados

Instâncias diferentes de um serviço de banco de dados podem conter um dado totalmente diferente, mesmo que sejam todos os mesmos tipos de serviço, geralmente chamados de classe de serviço. Para publicar esse tipo de serviço, o atributo **Keywords** do SCP pode identificar a classe de serviço e o banco de dados específico. Um cliente de uso geral que conhece apenas o GUID da classe de serviço pode consultar todos os bancos de dados publicados por essa classe de serviço e, em seguida, apresentar uma interface do usuário para permitir que o usuário selecione um. Para um cliente projetado especificamente para o banco de dados de destino, você pode embutir código na GUID do banco de dados no código do cliente.

## <a name="host-based-services"></a>Serviços baseados em host

Os serviços baseados em host são serviços que estão fortemente ligados a um único computador host. Você pode instalar instâncias da classe de serviço em vários computadores e cada instância fornece serviços que são identificados com seu computador host.

Cada instância de um serviço baseado em host deve criar seu próprio SCP no objeto de computador de seu host. Os clientes que usam um GUID de produto para pesquisar o SCP de um serviço baseado em host normalmente localizam muitas instâncias da classe de serviço em toda a floresta da empresa. Os clientes podem usar o atributo **serviceDNSName** do SCPs para localizar o scp para a instância de serviço no computador host desejado.

 

 