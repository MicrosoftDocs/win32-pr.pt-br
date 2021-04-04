---
description: O provedor WMI Core define classes que compõem a funcionalidade básica do WMI.
ms.assetid: 6EEA4284-CCFE-4206-9EAA-B4BCF988DE03
title: Provedor WMI Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9927be7208d9133d65257292950913972e96483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171098"
---
# <a name="wmi-core-provider"></a>Provedor WMI Core

O provedor WMI Core define classes que compõem a funcionalidade básica do WMI.

A maioria das classes do provedor WMI Core contém dados fornecidos pelo [provedor WDM](wdm-provider.md)e descreve monitores de exibição. As classes são definidas no WMI. mof e estão localizadas no namespace "root \\ WMI".

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                           | Descrição                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSMonitorClass**](msmonitorclass.md)<br/>                                             | é uma classe base WMI abstrata. As classes que descrevem os monitores de exibição de vídeo herdam deste [**MSMonitorClass**](msmonitorclass.md).<br/>                                                                         |
| [Classes MSMCA](msmca-classes.md)<br/>                                                   | um conjunto de classes WMI que expõem a arquitetura de verificação de máquina (MCA). A camada de abstração do sistema (SAL) fornece todos os eventos relatados na classe MSMCA. A Intel Corporation desenvolve e possui o MCA.<br/>         |
| [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md)<br/>                         | representa um contêiner para características de um intervalo de frequência com suporte.<br/>                                                                                                                                          |
| [**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)<br/>     | representa os recursos de exibição com suporte do monitor.<br/>                                                                                                                                                           |
| [**VideoModeDescriptor**](videomodedescriptor.md)<br/>                                   | contém elementos de descritor de modo para a matriz **MonitorSourceModes** na classe [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) .<br/>                                           |
| [**WMIEvent**](wmievent.md)<br/>                                                         | A classe [**WmiEvent**](wmievent.md) é uma classe base da qual todas as classes de evento WMI são derivadas.<br/>                                                                                                                |
| [**WmiMonitorAnalogVideoInputParams**](wmimonitoranalogvideoinputparams.md)<br/>         | representa os parâmetros de entrada de vídeo analógicos de um monitor de computador.<br/>                                                                                                                                                 |
| [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)<br/>                 | representa os recursos de exibição básicos de um monitor de computador.<br/>                                                                                                                                                        |
| [**WmiMonitorBrightness**](wmimonitorbrightness.md)<br/>                                 | representa os parâmetros de brilho de um monitor de computador.<br/>                                                                                                                                                         |
| [**WmiMonitorBrightnessEvent**](wmimonitorbrightnessevent.md)<br/>                       | representa uma alteração no brilho de um monitor.<br/>                                                                                                                                                                 |
| [**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)<br/>                   | contém métodos que gerenciam o brilho do monitor.<br/>                                                                                                                                                                    |
| [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md)<br/>             | representa as características de cor da CIE (Comissão Internacional de iluminação) de um monitor de computador.<br/>                                                                                                          |
| [**WmiMonitorConnectionParams**](wmimonitorconnectionparams.md)<br/>                     | contém o tipo de conexão do monitor.<br/>                                                                                                                                                                        |
| [**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)<br/>                   | contém métodos que obtêm o conteúdo bruto da definição de entrada de vídeo dos dados de identificação de vídeo avançado (VESA) avançados de associação de exibição estendida de vídeo (E-EDID) v. 1. x Standard 128-bytes de dados.<br/> |
| [**WmiMonitorDigitalVideoInputParams**](wmimonitordigitalvideoinputparams.md)<br/>       | representa parâmetros de entrada para vídeo digital.<br/>                                                                                                                                                                      |
| [**WmiMonitorID**](wmimonitorid.md)<br/>                                                 | representa as informações de identificação sobre um monitor de vídeo, como nome do fabricante, ano de fabricação ou número de série.<br/>                                                                                     |
| [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md)<br/>           | lista os intervalos de frequência com suporte no monitor.<br/>                                                                                                                                                                |
| [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md)<br/> | lista os modos de origem com suporte para um monitor de vídeo em seu descritor de monitor, se existir algum.<br/>                                                                                                                       |
| [**WmiMonitorRawEEdidV1Block**](wmimonitorraweedidv1block.md)<br/>                       | representa os dados brutos de uma estrutura de dados de identificação de exibição estendida (E-EDID) avançada de uma associação padrão de eletrônicos de vídeo (VESA).<br/>                                                                      |
| [**XYZinCIE**](xyzincie.md)<br/>                                                         | contém as coordenadas da exibição no espaço de cores da CIE (Comissão Internacional de iluminação) XYZ.<br/>                                                                                                      |



 

 

 




