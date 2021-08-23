---
title: Monitorar funções de configuração
description: Monitorar funções de configuração
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- monitor,functions
- monitor, funções de alto nível
- monitorar, funções de baixo nível
- monitor, funções de enumeração
- funções de alto nível
- funções de baixo nível
- funções de enumeração
- monitorar a configuração, funções
- monitorar a configuração, funções de alto nível
- monitorar configuração, funções de baixo nível
- monitorar configuração, funções de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b4eca3e18b5a5254ef9adc8cd55e123c26a773149d323caf517c5429d972f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013434"
---
# <a name="monitor-configuration-functions"></a>Monitorar funções de configuração

As funções a seguir são usadas para obter informações de um monitor e para alterar as configurações de um monitor. As funções de configuração do monitor são categorizadas em funções de alto nível, funções de baixo nível e funções de enumeração. Para obter mais informações, consulte [Using Monitor Configuration](using-monitor-configuration.md).

## <a name="high-level-functions"></a>High-Level funções



| Função                                                                         | Descrição                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**DegaussMonitor**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | Desgausse um monitor.                                                                 |
| [**GetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | Recupera as configurações de brilho mínimo, máximo e atual de um monitor.             |
| [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | Recupera os recursos de configuração de um monitor.                               |
| [**GetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | Recupera a temperatura de cor atual de um monitor.                                     |
| [**GetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | Recupera as configurações de contraste mínima, máxima e atual de um monitor.               |
| [**GetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | Recupera a posição horizontal ou vertical mínima, máxima e atual de um monitor. |
| [**GetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | Recupera a largura ou altura mínima, máxima e atual de um monitor.                 |
| [**GetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | Recupera o valor da unidade vermelho, verde ou azul de um monitor.                               |
| [**GetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | Recupera o valor de ganho vermelho, verde ou azul de um monitor.                                |
| [**GetMonitorTechnologyType**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | Recupera o tipo de tecnologia usado por um monitor.                                  |
| [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | Restaura as configurações de cor de um monitor para seus padrões de fábrica.                       |
| [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | Restaura as configurações de um monitor para seus padrões de fábrica.                             |
| [**SaveCurrentMonitorSettings**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | Salva as configurações atuais do monitor no armazenamento nãovolatile da exibição.             |
| [**SetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | Define o valor de brilho de um monitor.                                                   |
| [**SetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | Define a temperatura de cor de um monitor.                                                  |
| [**SetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | Define o valor de contraste de um monitor.                                                     |
| [**SetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | Define a posição horizontal ou vertical da área de exibição de um monitor.                |
| [**SetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | Define a largura ou a altura da área de exibição de um monitor.                                |
| [**SetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | Define o valor da unidade vermelho, verde ou azul de um monitor.                                    |
| [**SetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | Define o valor de ganho vermelho, verde ou azul de um monitor.                                     |



 

## <a name="low-level-functions"></a>Low-Level funções



| Função                                                                                   | Descrição                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | Recupera uma cadeia de caracteres que descreve os recursos de um monitor.                                                        |
| [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | Recupera o comprimento da cadeia de caracteres de funcionalidades de um monitor.                                                       |
| [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | Recupera as frequências de sincronização horizontal e vertical de um monitor.                                     |
| [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | Recupera o valor atual, o valor máximo e o tipo de código de um vcp (virtual Painel de Controle) para um monitor. |
| [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | Salva as configurações atuais do monitor no armazenamento nãovolatile da exibição.                                       |
| [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | Define o valor de um código Painel de Controle VCP (Virtual Painel de Controle) para um monitor.                                            |



 

## <a name="enumeration-functions"></a>Funções de enumeração



| Função                                                                                                   | Descrição                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | Fecha um alça para um monitor físico.                                                    |
| [**DestroyPhysicalMonitors**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | Fecha uma matriz de alças de monitor físico.                                              |
| [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | Recupera o número de monitores físicos associados a um guidão de monitor **HMONITOR.** |
| [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | Recupera o número de monitores físicos associados a um dispositivo Direct3D.              |
| [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | Recupera os monitores físicos associados a um guidão de monitor **HMONITOR.**           |
| [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | Recupera os monitores físicos associados a um dispositivo Direct3D.                        |



 

## <a name="internal-functions"></a>Funções internas

As funções a seguir são usadas pela API de configuração do monitor para acessar a funcionalidade no driver de exibição. Os aplicativos não devem chamar essas funções.

-   [**DDCCIGetCapabilitiesString**](ddccigetcapabilitiesstring.md)
-   [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md)
-   [**DDCCIGetTimingReport**](ddccigettimingreport.md)
-   [**DDCCIGetVCPFeature**](ddccigetvcpfeature.md)
-   [**DDCCISaveCurrentSettings**](ddccisavecurrentsettings.md)
-   [**DDCCISetVCPFeature**](ddccisetvcpfeature.md)
-   [**DestroyPhysicalMonitorInternal**](destroyphysicalmonitorinternal.md)
-   [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md)
-   [**GetPhysicalMonitorDescription**](getphysicalmonitordescription.md)
-   [**GetPhysicalMonitors**](getphysicalmonitors.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de configuração do Monitor](monitor-configuration-reference.md)
</dt> </dl>

 

 




