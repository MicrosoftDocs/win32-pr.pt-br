---
title: Usando as funções de configuração do monitor de Low-Level
description: Usando as funções de configuração do monitor de Low-Level
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- monitorar, funções
- monitorar, funções de configuração de nível baixo
- monitor, DDC/CI
- monitorar, exibir a interface de comando do canal de dados
- configurações do monitor, funções de configuração de nível baixo
- configuração do monitor, funções
- configuração do monitor, DDC/CI
- configuração do monitor, exibição da interface de comando do canal de dados
- funções de configuração de nível baixo
- Exibir interface de comando de canal de dados
- DDC/CI
- Conjunto de comandos de controle de monitor VESA (MCCS)
- Conjunto de comandos de controle de monitor (MCCS)
- MCCS (conjunto de comandos de controle de monitor)
- Painel de controle virtual (VCP)
- VCP (painel de controle virtual)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917248"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a>Usando as funções de configuração do monitor de Low-Level

Antes de usar as funções de configuração de monitor de nível baixo, você deve estar familiarizado com estes padrões:

-   Exibir a interface de comando do canal de dados (DDC/CI)
-   Conjunto de comandos de controle de monitor VESA (MCCS)

As funções de nível baixo funcionam obtendo e definindo os valores dos códigos do painel de controle virtual (VCP). Um código VCP pode ser *contínuo* ou não *contínuo*. Os códigos contínuos podem assumir qualquer valor entre zero e um valor máximo específico do fornecedor. Códigos não contínuos dão suporte a um conjunto definido de valores, que também são específicos para o fornecedor.

Para usar as funções de configuração do monitor de baixo nível, execute as seguintes etapas:

1.  Obtenha um identificador de **HMONITOR** chamando [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) ou [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).
2.  Chame [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) para obter o número de monitores físicos associados ao identificador **HMONITOR** .
3.  Chame [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) para obter uma lista de identificadores para os monitores físicos.
4.  Chame [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) para obter o comprimento da cadeia de caracteres de recursos DDC/CI de um monitor. A cadeia de caracteres de funcionalidades é uma cadeia de caracteres ASCII que contém informações estáticas sobre o monitor. Uma parte da cadeia de caracteres lista os códigos de VCP aos quais o monitor dá suporte. A cadeia de caracteres também lista os valores com suporte dos códigos VCP não contínuos.
5.  Aloque um buffer para manter a cadeia de caracteres de recursos e chame [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) para obter a cadeia de caracteres.
6.  Analise a cadeia de caracteres de funcionalidades para determinar quais códigos de VCP são compatíveis com o monitor.
7.  Para um código VCP contínuo, chame [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) para obter os valores atuais e máximos do código. Para um código VCP não contínuo, analise a cadeia de caracteres de funcionalidades para obter os valores com suporte.
8.  Chame [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) para definir um novo valor para um código VCP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando a configuração do monitor**](using-monitor-configuration.md)
</dt> </dl>

 

 