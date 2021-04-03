---
title: Replicação de partição de diretório de aplicativo
description: As partições de diretório de aplicativo são usadas com mais frequência para armazenar dados dinâmicos.
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- AD de replicação de partição de diretório de aplicativo
- Partições de diretório de aplicativos AD, replicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41523b86ae8d3a744d4eb288c5b240a60222aa21
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007364"
---
# <a name="application-directory-partition-replication"></a>Replicação de partição de diretório de aplicativo

As partições de diretório de aplicativo são usadas com mais frequência para armazenar dados dinâmicos. Como os dados são alterados com mais frequência do que os dados de configuração de uma floresta, o escopo de replicação e a frequência de uma partição de diretório de aplicativo podem ser definidos para cada partição. Os recursos de replicação do Active Directory Domain Services podem ser utilizados, mas os dados de replicação podem ser ajustados de acordo com o tipo de dados armazenados na partição.

O sistema operacional não impõe um número máximo de réplicas, mas o número de réplicas deve ser mantido em um mínimo para reduzir o impacto no desempenho da replicação dos dados da partição do diretório do aplicativo dinâmico.

O KCC gera e mantém a topologia de replicação para uma partição de diretório de aplicativos.

## <a name="application-directory-partition-replication-within-a-site"></a>Replicação de partição de diretório de aplicativo em um site

Os intervalos de replicação que controlam a replicação dentro do local de uma partição de diretório de aplicativos podem ser configurados. Isso permite que os dados dinâmicos em uma partição de diretório de aplicativo sejam sincronizados de forma mais imediata do que os dados mais estáticos em uma partição de domínio. Para obter mais informações sobre como configurar uma partição de diretório de aplicativo programaticamente, consulte [modificando a configuração de partição de diretório de aplicativo](modifying-application-directory-partition-configuration.md)

Dois atributos no objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) da partição de diretório do aplicativo e dois valores de registro em cada controlador de domínio do Windows 2000 e posterior controlam a latência de iniciar uma notificação de alteração originada para parceiros de replicação em um site.

-   O atributo [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay) de um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) especifica o atraso, em segundos, após a alteração de um objeto de origem antes que o primeiro parceiro de replicação seja notificado. Um valor de registro em cada controlador de domínio pode especificar um valor semelhante. Em uma floresta do Windows Server 2003, o primeiro atraso padrão é 15 segundos. Em uma floresta de modo misto, o primeiro atraso padrão é cinco minutos.
-   O atributo [**msDS-Replication-Notify-subseqüente-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) de um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) especifica o atraso, em segundos, entre as notificações subsequentes para o segundo, terceiro e assim em parceiros de replicação. Um valor de registro em cada controlador de domínio pode especificar um valor semelhante. Em uma floresta do Windows Server 2003, o atraso subsequente padrão é de 3 segundos. Em uma floresta de modo misto, o atraso subsequente padrão é de 30 segundos.

Os atributos [**crossRef**](/windows/desktop/ADSchema/c-crossref) se aplicam a todos os controladores de domínio que hospedam uma réplica da partição de diretório de aplicativo e afetam somente a replicação da partição de diretório de aplicativo identificada pelo objeto **crossRef** . Os valores do registro aplicam-se somente ao controlador de domínio no qual estão definidos e afetam a replicação entre sites para todas as partições que o controlador de domínio está hospedando. Se nem os atributos **crossRef** nem seus valores de registro estiverem definidos, um controlador de domínio usará os valores padrão. Se os valores do registro forem definidos, eles substituirão quaisquer valores definidos no objeto **crossRef** . Por padrão, os valores de registro e **crossRef** não são definidos, portanto, os valores padrão são usados. Isso permite que um administrador acelere a replicação para todas as réplicas de uma partição de diretório de aplicativo definindo os valores **crossRef** , ao mesmo tempo em que permite um ajuste mais preciso com as configurações do registro em cada controlador de domínio.

A partir do Windows Server 2003, as partições de domínio também usam esses atributos do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) para controlar a latência de replicação dentro do site. Essa é uma alteração das versões anteriores do servidor nas quais os intervalos de atraso foram controlados por valores de registro em cada controlador de domínio. Quando a floresta for atualizada para o Windows Server 2003, os valores de registro existentes serão preservados somente se tiverem sido modificados a partir dos valores padrão. Os intervalos de notificação dos controladores de domínio no registro substituem os intervalos de notificação armazenados no objeto **crossRef** da partição.

## <a name="application-directory-partition-replication-across-sites"></a>Replicação de partição de diretório de aplicativo entre sites

As réplicas de uma partição de diretório de aplicativo que estão localizadas em sites observam o agendamento de replicação entre sites como feito para a partição de domínio e a replicação de catálogo global. No entanto, as réplicas de uma partição de diretório de aplicativo são mais frequentemente localizadas em um site ao hospedar dados verdadeiramente voláteis porque a latência de replicação entre sites pode não ser aceitável para que as réplicas sejam consistentes entre si.

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>As partições de diretório de aplicativo não são replicadas para catálogos globais

Os objetos em uma partição de diretório de aplicativo não são replicados para o catálogo global. A partição de diretório de aplicativo é provisionada como Hospedagem de dados e objetos dinâmicos para os quais não pode ser sensato, nem é possível replicar os objetos de forma ampla. Por esse motivo, a partição de diretório de aplicativos oferece escopo controlado e frequência de replicação. Por isso, não há motivo para permitir que esses objetos sejam replicados para o catálogo global e, portanto, sejam distribuídos em toda a floresta onde existe um servidor de catálogo global. Isso não restringe objetos em uma partição de diretório de aplicativo do uso de atributos no esquema marcado como [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset). Assim como ocorre com qualquer controlador de domínio, um servidor de catálogo global ainda pode ser configurado para ser uma réplica completa de uma partição de diretório de aplicativo.

 

 