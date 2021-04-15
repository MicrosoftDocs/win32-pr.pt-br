---
description: O Integration Services são serviços de software que são executados sobre o sistema operacional convidado dentro de uma máquina virtual filho e como parte da pilha de virtualização no sistema operacional de gerenciamento para fornecer algum nível de integração com o sistema operacional de gerenciamento.
ms.assetid: 7A8E9EF2-AC67-47CB-81A5-BF4C8A55D710
title: Classes do Integration Services
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04d60a913159c49387848b5e18a3e37b942f3e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502372"
---
# <a name="integration-services-classes"></a>Classes do Integration Services

O Integration Services são serviços de software que são executados sobre o sistema operacional convidado dentro de uma máquina virtual filho e como parte da pilha de virtualização no sistema operacional de gerenciamento para fornecer algum nível de integração com o sistema operacional de gerenciamento. Eles são usados para solucionar problemas que surgem do alto nível de isolamento fornecido pelas máquinas virtuais.

Veja a seguir as classes WMI de virtualização relacionadas ao Integration Services.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                | Descrição                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)<br/>                                               | Representa um trabalho de operação do serviço de arquivo convidado. <br/>                                                                                                                                                                                                            |
| [**Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)<br/>                               | Representa os parâmetros para copiar um arquivo do host para o convidado. <br/>                                                                                                                                                                                |
| [**Msvm \_ GuestFileService**](msvm-guestfileservice.md)<br/>                                                   | [**Msvm \_ GuestFileService**](msvm-guestfileservice.md) contém um método que pode ser usado para copiar um arquivo para uma máquina virtual do host Hyper-V. <br/>                                                                                                     |
| [**Msvm \_ GuestService**](msvm-guestservice.md)<br/>                                                           | [**Msvm \_ GuestService**](msvm-guestservice.md) é a classe base abstrata para serviços no convidado que podem ser acessados do host. <br/>                                                                                                                  |
| [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)<br/>                       | Representa o estado do componente de interface do serviço de convidado, que fornece um mecanismo para interagir com a máquina virtual a partir das interfaces de gerenciamento no sistema host. <br/>                                                                         |
| [**Msvm \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)<br/> | Representa o estado configurado do componente de interface do serviço de convidado. <br/>                                                                                                                                                                                 |
| [**Msvm \_ KvpExchangeComponent**](msvm-kvpexchangecomponent.md)<br/>                                           | Representa o estado do serviço de troca de pares chave/valor, que fornece um mecanismo para trocar dados entre a máquina virtual e o sistema operacional em execução no sistema operacional de gerenciamento.<br/>                                                  |
| [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)<br/>                     | Representa o estado configurado do serviço de troca de pares chave/valor.<br/>                                                                                                                                                                                    |
| [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)<br/>                                             | Representa um par de chave/valor.<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ RegisteredGuestService**](msvm-registeredguestservice.md)<br/>                                       | Representa uma associação entre uma instância de [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) e uma instância de [**Msvm \_ GuestService**](msvm-guestservice.md), que representa um serviço em execução no convidado. <br/> |
| [**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)<br/>                                                 | Representa o estado do serviço de desligamento, que fornece um mecanismo para desligar o sistema operacional da máquina virtual das interfaces de gerenciamento no sistema host.<br/>                                                                       |
| [**Msvm \_ ShutdownComponentSettingData**](msvm-shutdowncomponentsettingdata.md)<br/>                           | Representa o estado configurado do serviço de desligamento.<br/>                                                                                                                                                                                                   |
| [**Msvm \_ TimeSyncComponent**](msvm-timesynccomponent.md)<br/>                                                 | Representa o estado do serviço de sincronização de tempo, que é responsável por sincronizar a hora do sistema de uma máquina virtual com a hora do sistema operacional em execução no sistema operacional de gerenciamento.<br/>                             |
| [**Msvm \_ TimeSyncComponentSettingData**](msvm-timesynccomponentsettingdata.md)<br/>                           | Representa o estado configurado do serviço de sincronização de tempo.<br/>                                                                                                                                                                                       |
| [**Msvm \_ VssComponent**](msvm-vsscomponent.md)<br/>                                                           | Representa o estado do serviço de Serviço de Cópias de Sombra de Volume (VSS), que implementa o solicitante VSS no sistema operacional convidado.<br/>                                                                                                                    |
| [**Msvm \_ VssComponentSettingData**](msvm-vsscomponentsettingdata.md)<br/>                                     | Representa o estado configurado do serviço de Serviço de Cópias de Sombra de Volume (VSS).<br/>                                                                                                                                                                           |



 

 

 




