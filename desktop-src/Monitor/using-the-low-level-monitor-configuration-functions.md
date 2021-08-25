---
title: Usando as funções de configuração Low-Level Monitor
description: Usando as funções de configuração Low-Level Monitor
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- monitor,functions
- monitor, funções de configuração de baixo nível
- monitor,DDC/CI
- monitor, Exibir Interface de Comando do Canal de Dados
- monitorar configuração, funções de configuração de baixo nível
- monitorar a configuração, funções
- monitorar a configuração, DDC/CI
- monitorar configuração, Exibir Interface de Comando do Canal de Dados
- funções de configuração de baixo nível
- Exibir interface de comando do canal de dados
- DDC/CI
- CONJUNTO de Comandos de Controle do VESA Monitor (MCCS)
- Monitor Control Command Set (MCCS)
- MCCS (Monitor Control Command Set)
- VCP (Painel de Controle virtual)
- VCP (Virtual Painel de Controle)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ffd21f0b232db71bb6023f968122271ce70f03b0a632dc33d9df1e7ee993bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927386"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a>Usando as funções de configuração Low-Level Monitor

Antes de usar as funções de configuração de monitor de baixo nível, você deve estar familiarizado com estes padrões:

-   DDC/CI (Interface de Comando do Canal de Dados de Exibição)
-   CONJUNTO de Comandos de Controle do VESA Monitor (MCCS)

As funções de baixo nível funcionam ao obter e definir os valores de códigos Painel de Controle VCP (Virtual Painel de Controle). Um código VCP pode *ser contínuo* ou *não contínuo.* Códigos contínuos podem assumir qualquer valor entre zero e um valor máximo específico do fornecedor. Códigos não continuados suportam um conjunto definido de valores, que também é específico para o fornecedor.

Para usar as funções de configuração de monitor de baixo nível, execute as seguintes etapas:

1.  Obtenha um **alça HMONITOR** chamando [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) ou [**MonitorFromWindow.**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)
2.  Chame [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) para obter o número de monitores físicos associados ao alça **HMONITOR.**
3.  Chame [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) para obter uma lista de alças para os monitores físicos.
4.  Chame [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) para obter o comprimento da cadeia de caracteres de recursos de DDC/CI de um monitor. A cadeia de caracteres de funcionalidades é uma cadeia de caracteres ASCII que contém informações estáticas sobre o monitor. Uma parte da cadeia de caracteres lista os códigos VCP aos qual o monitor dá suporte. A cadeia de caracteres também lista os valores com suporte dos códigos VCP não continuados.
5.  Aloce um buffer para manter a cadeia de caracteres de funcionalidades e chame [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) para obter a cadeia de caracteres.
6.  Analisar a cadeia de caracteres de funcionalidades para determinar a quais códigos VCP o monitor dá suporte.
7.  Para um código VCP contínuo, chame [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) para obter os valores atuais e máximos do código. Para um código VCP nãocontinuos, analisar a cadeia de caracteres de funcionalidades para obter os valores com suporte.
8.  Chame [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) para definir um novo valor para um código VCP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando a configuração do Monitor**](using-monitor-configuration.md)
</dt> </dl>

 

 