---
description: Um conjunto de classes WMI que expõem a arquitetura de verificação de máquina (MCA). A camada de abstração do sistema (SAL) fornece todos os eventos relatados na classe MSMCA. A Intel Corporation desenvolve e possui o MCA.
ms.assetid: 4e35f871-5bce-49ed-a3e8-d2d967e6e2dc
title: Classes MSMCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461d4c5c50ae5316c96c3dffc18af7b729cfa6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297060"
---
# <a name="msmca-classes"></a>Classes MSMCA

As classes MSMCA (arquitetura de verificação de máquina da Microsoft) são um conjunto de classes WMI que expõem a arquitetura de verificação de máquina (MCA). A camada de abstração do sistema (SAL) fornece todos os eventos relatados na classe MSMCA. A Intel Corporation desenvolve e possui o MCA.



| Classe                                                                               | Descrição                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**MSMCAEvent \_ CPUError**](msmcaevent-cpuerror.md)                                 | Representa um evento de erro de CPU.                                                                          |
| [**\_Cabeçalho MSMCAEvent**](msmcaevent-header.md)                                     | Representa o cabeçalho comum que todas as classes MSMCAEvent usam.                                          |
| [**MSMCAEvent \_ InvalidError**](msmcaevent-invaliderror.md)                         | Representa um erro inválido da arquitetura de verificação de memória (MCA).                                            |
| [**MSMCAEvent \_ MemoryError**](msmcaevent-memoryerror.md)                           | Representa um evento de erro de memória MCA.                                                                  |
| [**MSMCAEvent \_ MemoryPageRemoved**](msmcaevent-memorypageremoved.md)               | Indica que o sistema operacional removeu uma página física de memória.                                 |
| [**MSMCAEvent \_ PCIBusError**](msmcaevent-pcibuserror.md)                           | Representa um erro de barramento PCI MCA.                                                                       |
| [**MSMCAEvent \_ PCIComponentError**](msmcaevent-pcicomponenterror.md)               | Representa um erro de componente de PCI MCA.                                                                 |
| [**MSMCAEvent \_ PlatformSpecificError**](msmcaevent-platformspecificerror.md)       | Representa um erro específico da plataforma MCA.                                                             |
| [**MSMCAEvent \_ SMBIOSError**](msmcaevent-smbioserror.md)                           | Representa um erro de BIOS do sistema MCA.                                                                   |
| [**MSMCAEvent \_ SwitchToCMCPolling**](msmcaevent-switchtocmcpolling.md)             | Indica que o tratamento de verificação de máquina corrigido foi alternado para sondagem.                            |
| [**MSMCAEvent \_ SystemEventError**](msmcaevent-systemeventerror.md)                 | Representa um erro de evento do sistema MCA.                                                                  |
| [**MSMCAInfo**](msmcainfo.md)                                                      | Classe base abstrata da qual todas as classes de dados do provedor de arquitetura de verificação de máquina (MCA) são derivadas. |
| [**\_Entrada MSMCAInfo**](msmcainfo-entry.md)                                         | Representa uma entrada de informações de MCA, verificação de máquina corrigida (CMC) ou erro de plataforma corrigido (CPE). |
| [**MSMCAInfo \_ RawCMCEvent**](msmcainfo-rawcmcevent.md)                             | Contém um evento CMC.                                                                                  |
| [**MSMCAInfo \_ RawCorrectedPlatformEvent**](msmcainfo-rawcorrectedplatformevent.md) | Contém um evento de plataforma corrigido.                                                                   |
| [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md)                               | Especifica os logs MCA brutos.                                                                            |
| [**MSMCAInfo \_ RawMCAEvent**](msmcainfo-rawmcaevent.md)                             | Contém um evento MCA.                                                                                  |
| [**WmiEvent**](wmievent.md)                                                        | Classe base abstrata da qual todas as classes de evento do provedor MCA são derivadas.                             |



 

 

 



