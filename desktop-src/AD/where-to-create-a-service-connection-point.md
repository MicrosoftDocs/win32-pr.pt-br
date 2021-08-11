---
title: Onde criar um ponto de conexão de serviço
description: Quando uma instância do Active Directory Domain Services é instalada, o instalador do serviço cria objetos do ponto de conexão de serviço (SCP) no Active Directory Domain Services.
ms.assetid: a90566d9-dd68-43e2-be9e-300d57a7fbf4
ms.tgt_platform: multiple
keywords:
- onde criar um anúncio de ponto de conexão de serviço
- Active Directory, onde criar um ponto de conexão de serviço
- onde criar um anúncio de ponto de conexão de serviço
- Criando um AD de ponto de conexão de serviço
- AD de ponto de conexão de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b585c11333b8e307a7f6771bd89ccf5ad82038fb22f10fca7eb114c1101a063a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182075"
---
# <a name="where-to-create-a-service-connection-point"></a>Onde criar um ponto de conexão de serviço

Quando uma instância do Active Directory Domain Services é instalada, o instalador do serviço cria objetos do ponto de conexão de serviço (SCP) no Active Directory Domain Services. O objetivo principal deve ser minimizar o tráfego de replicação e habilitar a administração e a manutenção eficientes dos objetos.

Lembre-se de que os aplicativos cliente localizam SCPs pesquisando no diretório as palavras-chave no SCP. O atributo de **palavras-chave** de um SCP está incluído no catálogo global; Os clientes podem pesquisar o catálogo global para localizar SCPs na floresta. Por esse motivo, o cliente não influencia onde publicar SCPs.

## <a name="minimize-replication-traffic"></a>Minimizar o tráfego de replicação

Para minimizar o tráfego de replicação, crie SCPs na partição de domínio do domínio do computador host de serviço. Por exemplo, você pode criar SCPs como objetos filho do objeto de computador no qual o serviço está instalado. Uma partição de domínio de Active Directory Domain Services, às vezes chamada de contexto de nomenclatura de domínio, contém objetos específicos de domínio, como os objetos para os usuários e computadores do domínio. Uma réplica completa de todos os objetos na partição de domínio é replicada para cada controlador de domínio (DC) para o domínio, mas não é replicada para os DCs de outros domínios.

Não crie SCPs na partição de configuração, também conhecida como o contexto de nomenclatura de configuração, porque as alterações na partição de configuração são replicadas para cada DC na floresta. Conforme observado acima, os clientes em toda a floresta podem consultar o catálogo global para localizar SCPs em qualquer lugar da floresta, portanto, criar SCPs na partição de configuração não os torna mais visíveis para os clientes; Ele só gera mais tráfego de replicação.

## <a name="ease-of-administration"></a>Facilidade de administração

Considere as seguintes diretrizes para a administração de objetos:

-   Coloque os objetos específicos do serviço em que os administradores possam controlar o acesso a eles usando políticas e permissões de acesso herdadas.
-   Coloque os objetos em que um administrador possa encontrá-los facilmente.

Um bom local padrão que satisfaz ambas as metas é criar o SCP e outros objetos específicos de serviço no objeto de computador do computador host de cada instância de serviço. Para obter mais informações, consulte [publicação em um objeto de computador](publishing-under-a-computer-object.md).

Uma boa alternativa para os serviços não vinculados a um único host é criar um contêiner para os objetos de serviço no contêiner do sistema em uma partição de domínio. Para obter mais informações, consulte [publicando em um contêiner do sistema de domínio](publishing-in-a-domain-system-container.md).

O diagrama a seguir mostra parte da hierarquia de contêiner padrão para uma partição de domínio.

![hierarquia de contêiner de partição de domínio padrão](images/domain-container-heirarchy.png)

O diagrama mostra a hierarquia de domínio padrão incluída com Active Directory Domain Services. No entanto, muitas empresas criam uma hierarquia de contêineres de UO (unidade organizacional) para agrupar classes de objetos, como usuários e computadores, para fins de administração. Os administradores podem aplicar políticas e ACEs (entradas de controle de acesso) herdáveis a uma UO para delegar autoridade administrativa para objetos na UO. Isso permite que os administradores gerenciem com eficiência uma empresa, mas tem algumas consequências para programadores de serviço:

-   O objeto de computador para um host de serviço pode não estar no contêiner computadores, conforme mostrado no diagrama. Para obter mais informações sobre como localizar o objeto de computador para o computador local, consulte [publicando em um objeto Computer](publishing-under-a-computer-object.md).
-   Os administradores podem mover objetos conforme suas necessidades organizacionais mudam. Isso significa que você não pode depender de seus objetos restantes em um local fixo; ou seja, o serviço não pode depender de um nome diferenciado de objeto restante do mesmo. Em vez disso, use o atributo **objectGUID** de um objeto, que não será alterado se o objeto for movido ou renomeado. Para obter mais informações, e um exemplo de código que cria um SCP, armazena seu **objectGUID** e, posteriormente, recupera o **objectGUID** para associar ao scp, consulte [criando e mantendo um ponto de conexão de serviço](creating-and-maintaining-a-service-connection-point.md).
-   Todas as classes de objeto relacionadas ao serviço padrão, bem como quaisquer subclasses dessas classes, são filhos válidos das classes **Computer** e **OrganizationalUnit** . Se você estender o esquema para definir sua própria classe específica de serviço, certifique-se de que as classes **Computer** e **OrganizationalUnit** estejam incluídas nos superiores possíveis.
-   O instalador do serviço determina o local padrão para a criação de SCPs. Talvez você queira permitir que o administrador instale o serviço para especificar um caminho de instalação alternativo.

Os objetos específicos do serviço não devem ser criados nas seguintes áreas:

-   Os serviços não devem publicar objetos diretamente nos contêineres usuários ou computadores de uma partição de domínio, nem devem criar novos contêineres nesses contêineres. No entanto, os serviços podem publicar objetos como objetos filho de um objeto de computador, independentemente de o objeto de computador estar ou não armazenado no contêiner computadores.
-   os serviços que Windows usam o RnR (registro e resolução de soquetes) ou as APIs de serviço de nome RPC (RpcNs) para se anunciar, criam os objetos apropriados nos contêineres winsockservices e RpcServices no contêiner do sistema de uma partição de domínio. Não crie objetos explicitamente nesses contêineres. Fazer isso não causa danos diretos, mas pode ser confuso para os administradores.

 

 




