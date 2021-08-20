---
description: Microsoft Hyper-V servidor fornece um ambiente de gerenciamento de máquina virtual escalonável, confiável e altamente disponível. O software de máquina virtual hyper-V consolida servidores e ambientes de desenvolvimento e teste.
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: Provedor WMI do Hyper-V (V2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82156754f085196eaece86bb4996c1b4a0bb8348e1566894ee78d4921676f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014244"
---
# <a name="hyper-v-wmi-provider-v2"></a>Provedor WMI do Hyper-V (V2)

## <a name="purpose"></a>Finalidade

O Hyper-V fornece um ambiente de computação de servidor virtualizado escalonável, confiável e altamente disponível. Ele permite que um ou mais sistemas operacionais convidados executem simultaneamente em um único computador físico. Os principais usos da tecnologia de máquina virtual incluem o seguinte:

-   Consolidação de servidor
-   Consolidação de ambientes de desenvolvimento e teste
-   Recuperação de desastre simplificada

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                 | Descrição                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre o provedor WMI do Hyper-V](about-the-virtualization-wmi-provider.md)<br/>                | O provedor WMI para Hyper-V permite que desenvolvedores e criadores de script criem rapidamente ferramentas personalizadas, utilitários e aprimoramentos para a plataforma de virtualização. As interfaces WMI podem gerenciar todos os aspectos dos serviços do Hyper-V.<br/> |
| [Usando o provedor WMI do Hyper-V](using-the-virtualization-wmi-provider.md)<br/>                | Os tópicos a seguir descrevem como usar o provedor WMI do Hyper-V.<br/>                                                                                                                                                            |
| [Classes WMI do Hyper-V](hyper-v-wmi-classes.md)<br/>                                             | A seguir estão as classes WMI do Hyper-V.<br/>                                                                                                                                                                                    |
| [API de monitoramento de saúde do aplicativo Hyper-V](hyper-v-application-health-monitoring-api.md)<br/> | A API de monitoramento de saúde do aplicativo Hyper-V é usada para monitorar o estado de saúde dos aplicativos em execução em uma máquina virtual.<br/>                                                                                               |
| [API de replicação do Hyper-V](hyper-v-replication-api.md)<br/>                                     | A API de replicação do Hyper-V é usada para controlar a replicação de máquina virtual e a recuperação de failover.<br/>                                                                                                                             |
| [API de métricas do Hyper-V](hyper-v-metrics-api.md)<br/>                                             | A API de métricas do Hyper-V é usada para monitorar o estado de saúde dos aplicativos em execução em uma máquina virtual.<br/>                                                                                                                     |
| [API de rede hyper-V](hyper-v-networking-api.md)<br/>                                       | A API de rede hyper-V é usada para controlar a rede no Hyper-V.<br/>                                                                                                                                                          |
| [API de migração do Hyper-V](hyper-v-storage-migration-api.md)<br/>                                 | A API de migração do Hyper-V é usada para controlar o armazenamento e a migração ao vivo no Hyper-V.<br/>                                                                                                                                           |
| [Hyper-V virtual Fibre Channel API](hyper-v-virtual-fiber-channels-api.md)<br/>                | A API de Fibre Channel virtual do Hyper-V é usada para controlar adaptadores Fibre Channel virtuais no Hyper-V.<br/>                                                                                                                           |
| [API de posicionamento de VM do Hyper-V](hyper-v-vm-placement-api.md)<br/>                                   | A API de posicionamento da VM (máquina virtual) do Hyper-V contém as informações de compatibilidade para as VMs ou o sistema de computador de hospedagem.<br/>                                                                                                        |
| [Classes de limite](threshold-classes.md)<br/>                                                 | Contém as classes introduzidas no Windows 10.<br/>                                                                                                                                                                                |
| [RS2 Classes](redstone-classes.md)<br/>                                                        | Contém as novas classes para Windows 10, versão 1703.<br/>                                                                                                                                                                        |
| [RS3 Classes](rs3-classes.md)<br/>                                                             | Contém as novas classes para Windows 10, versão 1709.<br/>                                                                                                                                                                        |
| [Glossário do Hyper-V](virtualization-glossary.md)<br/>                                            | Glossário de termos usados na documentação Windows do SDK de Virtualização.<br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Os serviços hyper-V exigem um sistema baseado em x64 que dá suporte à virtualização assistida por hardware que executa o Hyper-V. No entanto, os programas que interagem com as interfaces WMI do Hyper-V podem ser executados remotamente em qualquer sistema que dá suporte ao WMI.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hyper-V (biblioteca técnica Windows Server 2008 R2)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))
</dt> <dt>

[Instrumentação de Gerenciamento do Windows](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[Virtualização do Windows Server](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

