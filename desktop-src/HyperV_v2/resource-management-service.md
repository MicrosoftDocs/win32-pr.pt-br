---
description: O perfil de virtualização de recursos fornece os meios pelos quais um cliente pode descobrir os recursos virtuais com suporte no sistema de virtualização.
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: Serviço de gerenciamento de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c405cac60df719195466da6ea0c7aadb7bf0d765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011637"
---
# <a name="resource-management-service"></a>Serviço de gerenciamento de recursos

O perfil de virtualização de recursos fornece os meios pelos quais um cliente pode descobrir os recursos virtuais com suporte no sistema de virtualização. Ele também descreve a capacidade — ou o número de alocações — que tem suporte para cada tipo de recurso virtual. A ilustração a seguir mostra o perfil de virtualização de recursos.

![Perfil de virtualização de recursos](images/resourcemanagement.png)

Duas classes diferentes de recursos virtuais são definidas pelo perfil de virtualização de recursos:

-   Recurso compartilhado: representa os recursos do host que estão ou são capazes de serem compartilhados entre várias máquinas virtuais. [**Msvm \_ O processador**](msvm-processor.md) é um exemplo de um recurso compartilhado.
-   Recurso sintético: representa os recursos virtuais que não têm nenhum recurso de host correspondente. [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) é um exemplo de um recurso sintético.

O pool de recursos é usado para coletar uma classe de recursos de host para que possa ser facilmente descoberto, enquanto seus recursos e configurações podem ser descritos em um local central. Não há nenhum limite para a forma como é básica ou avançada uma implementação do recurso coletado.

No pool de recursos, o cliente pode acessar os recursos de alocação associados (AC). Essa classe descreve os recursos do recurso descrito por esse pool de recursos. Por exemplo, isso pode indicar se o [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) representado por esse pool de recursos dá suporte a VLANs (redes virtuais) ou filtros.

O perfil AC define o meio pelo qual um cliente pode descobrir o intervalo válido de e as configurações padrão para um determinado recurso virtual. Um objeto AC está associado a cada pool de recursos. Quatro objetos RASD (dados de configuração de alocação de recursos) estão associados ao objeto AC para descrever os valores mínimo, máximo, padrão e incremental para a alocação do recurso fornecido. Juntas, essas classes descrevem o intervalo geral de recursos com suporte. A instância [**Msvm \_ AllocationCapabilities**](msvm-allocationcapabilities.md) fornece um ponto de ancoragem para o conjunto de instâncias de [**\_ ResourceAllocationSettingData do Msvm**](msvm-resourceallocationsettingdata.md) que especificam o intervalo padrão e válido de configurações para um recurso virtual. A classe de associação [**Msvm \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) fornece o link entre a instância AC e as configurações mínima, máxima, incremental e padrão para um recurso suportado pela plataforma de virtualização.

 

 



