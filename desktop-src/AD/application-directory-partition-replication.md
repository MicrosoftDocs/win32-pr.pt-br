---
title: Replicação de partição do Diretório do Aplicativo
description: As partições de diretório do aplicativo são usadas com mais frequência para armazenar dados dinâmicos.
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- AD de Replicação de Partição do Diretório do Aplicativo
- Partições do diretório de aplicativos AD, Replicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7df6c50653fe1660bbf95f0f6ca580404d38c366c1045bc3d1b712ca771d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024406"
---
# <a name="application-directory-partition-replication"></a>Replicação de partição do Diretório do Aplicativo

As partições de diretório do aplicativo são usadas com mais frequência para armazenar dados dinâmicos. Como os dados mudam com mais frequência do que os dados de configuração de uma floresta, o escopo de replicação e a frequência de uma partição de diretório do aplicativo podem ser definidos para cada partição. Os recursos de replicação Active Directory Domain Services podem ser utilizados, mas os dados de replicação podem ser ajustados para se adequar ao tipo de dados armazenados na partição.

O sistema operacional não impõe um número máximo de réplicas, mas o número de réplicas deve ser mantido no mínimo para reduzir o impacto no desempenho da replicação dos dados de partição do diretório de aplicativo dinâmico.

O KCC gera e mantém a topologia de replicação para uma partição de diretório do aplicativo.

## <a name="application-directory-partition-replication-within-a-site"></a>Replicação de partição do diretório do aplicativo em um site

Os intervalos de replicação que controlam a replicação dentro do site de uma partição de diretório do aplicativo podem ser configurados. Isso permite que os dados dinâmicos em uma partição de diretório de aplicativo sejam sincronizados mais rapidamente do que os dados mais estáticos em uma partição de domínio. Para obter mais informações sobre como configurar programaticamente uma partição de diretório do aplicativo, consulte [Modificando a configuração de partição do diretório do aplicativo.](modifying-application-directory-partition-configuration.md)

Dois atributos no objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) da partição do diretório do aplicativo e dois valores de Registro em cada controlador de domínio Windows 2000 e posterior controlam a latência de iniciar uma notificação de alteração originada para parceiros de replicação em um site.

-   O atributo [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay) de um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) especifica o atraso, em segundos, após uma alteração de objeto de origem antes que o primeiro parceiro de replicação seja notificado. Um valor do Registro em cada controlador de domínio pode especificar um valor semelhante. Em uma Windows Server 2003, o primeiro atraso padrão é de 15 segundos. Em uma floresta de modo misto, o primeiro atraso padrão é de cinco minutos.
-   O atributo [**msDS-Replication-Notify-Subsequent-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) de um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) especifica o atraso, em segundos, entre as notificações subsequentes para o segundo, o terceiro e assim por diante nos parceiros de replicação. Um valor do Registro em cada controlador de domínio pode especificar um valor semelhante. Em uma Windows Server 2003, o atraso subsequente padrão é de 3 segundos. Em uma floresta de modo misto, o atraso subsequente padrão é de 30 segundos.

Os [**atributos crossRef**](/windows/desktop/ADSchema/c-crossref) se aplicam a todos os controladores de domínio que hospedam uma réplica da partição de diretório do aplicativo e afetam apenas a replicação da partição de diretório do aplicativo identificada pelo **objeto crossRef.** Os valores do Registro se aplicam somente ao controlador de domínio no qual eles estão definidos e afetam a replicação intra-site para todas as partições que o controlador de domínio está hospedando. Se nem os **atributos crossRef** nem seus valores de Registro são definidos, um controlador de domínio usa os valores padrão. Se os valores do Registro são definidos, eles substituem os valores definidos no **objeto crossRef.** Por padrão, os valores de registro e **crossRef** não são definidos, portanto, os valores padrão são usados. Isso permite que um administrador acelere a replicação para todas as réplicas de uma partição de diretório de aplicativo definindo os valores **crossRef,** permitindo um ajuste mais fino com as configurações do Registro em cada controlador de domínio.

A partir do Windows Server 2003, as partições de domínio também usam esses atributos do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) para controlar a latência de replicação dentro do site. Essa é uma alteração das versões anteriores do servidor em que os intervalos de atraso eram controlados pelos valores do Registro em cada controlador de domínio. Quando a floresta é atualizada para o Windows Server 2003, os valores do Registro existentes são preservados somente se eles foram modificados dos valores padrão. Os intervalos de notificação dos controladores de domínio no Registro substituem os intervalos de notificação armazenados no objeto **de partição crossRef.**

## <a name="application-directory-partition-replication-across-sites"></a>Replicação de partição do diretório de aplicativos entre sites

As réplicas de uma partição de diretório de aplicativo localizada entre sites observam o agendamento de replicação entre sites, conforme feito para a partição de domínio e a replicação de catálogo global. No entanto, as réplicas de uma partição de diretório de aplicativo são localizadas com mais frequência dentro de um site ao hospedar dados realmente voláteis porque a latência de replicação entre sites pode não ser aceitável para fazer com que as réplicas sejam consistentes entre si.

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>As partições do diretório do aplicativo não são replicadas para catálogos globais

Objetos em uma partição de diretório de aplicativo não são replicados para o catálogo global. A partição do diretório do aplicativo é prevista como hospedando dados dinâmicos e objetos para os quais não pode ser razoável nem viável replicar os objetos amplamente. Por esse motivo, a partição de diretório do aplicativo oferece escopo controlado e frequência de replicação. Por isso, não há motivo para permitir que esses objetos sejam replicados no catálogo global e, portanto, sejam distribuídos em toda a floresta em que existe um servidor de catálogo global. Isso não restringe objetos em uma partição de diretório de aplicativo de usar atributos no esquema marcado como [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset). Assim como com qualquer controlador de domínio, um servidor de catálogo global ainda pode ser configurado para ser uma réplica completa de uma partição de diretório do aplicativo.

 

 