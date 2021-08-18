---
description: O Perfil de Virtualização de Recursos fornece os meios pelos quais um cliente pode descobrir os recursos virtuais com suporte pelo sistema de virtualização.
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: Serviço de gerenciamento de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593af3c440ad15add50445a3b05f41d44c8c396a1334635aeaf141838e82e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746207"
---
# <a name="resource-management-service"></a>Serviço de gerenciamento de recursos

O Perfil de Virtualização de Recursos fornece os meios pelos quais um cliente pode descobrir os recursos virtuais com suporte pelo sistema de virtualização. Ele também descreve a capacidade ou o número de alocações com suporte para cada tipo de recurso virtual. A ilustração a seguir mostra o Perfil de Virtualização de Recursos.

![perfil de virtualização de recursos](images/resourcemanagement.png)

Duas classes diferentes de recursos virtuais são definidas pelo Perfil de Virtualização de Recursos:

-   Recurso Compartilhado: representa os recursos do host que são ou podem ser compartilhados entre várias máquinas virtuais. [**Msvm \_ Processador**](msvm-processor.md) é um exemplo de um recurso compartilhado.
-   Recurso sintético: representa os recursos virtuais que não têm nenhum recurso de host correspondente. [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) é um exemplo de um recurso sintético.

O pool de recursos é usado para coletar uma classe de recursos de host para que ele possa ser facilmente descoberto, enquanto seus recursos e configurações podem ser descritos em um local central. Não há nenhum limite para o quão básica ou avançada uma implementação do recurso coletado pode ser.

No pool de recursos, o cliente pode acessar as AC (capacidades de alocação) associadas. Essa classe descreve os recursos do recurso descrito por esse pool de recursos. Por exemplo, pode indicar se o [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) representado por esse pool de recursos dá suporte a VLANs (VLANs) virtuais ou filtros.

O Perfil ac define os meios pelos quais um cliente pode descobrir o intervalo válido de e as configurações padrão para um determinado recurso virtual. Um objeto AC é associado a cada pool de recursos. Quatro objetos RASD (Dados de Configuração de Alocação de Recursos) são associados ao objeto AC para descrever os valores mínimo, máximo, padrão e incremental para a alocação do recurso determinado. Juntas, essas classes descrevem a gama geral de recursos com suporte. A [**instância Msvm \_ AllocationCapabilities**](msvm-allocationcapabilities.md) fornece um ponto de âncora para o conjunto de instâncias [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que especificam o intervalo padrão e válido de configurações para um recurso virtual. A classe de associação [**Msvm \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) fornece o link entre a instância ac e as configurações mínimas, máximas, incrementais e padrão para um recurso com suporte pela plataforma de virtualização.

 

 



