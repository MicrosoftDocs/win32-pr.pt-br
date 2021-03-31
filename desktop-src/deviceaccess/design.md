---
title: Considerações de design para dispositivos personalizados
description: Este tópico descreve as considerações de design que podem ajudá-lo a determinar se o dispositivo precisa de um driver personalizado.
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: f503ae556009f3b4b9b88d9f895936218f402fc6
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103642954"
---
# <a name="design-considerations-for-custom-devices"></a>Considerações de design para dispositivos personalizados

Este tópico descreve as considerações de design que podem ajudá-lo a determinar se o dispositivo precisa de um driver personalizado.

- [Determinando o tipo de driver a ser implementado](#determining-the-type-of-driver-to-implement)
- [Considerações sobre segurança](#security-considerations)
- [Tópicos relacionados](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>Determinando o tipo de driver a ser implementado

Esta tabela descreve quando você deve desenvolver um driver personalizado para seu dispositivo e se comunicar com ele usando a API de acesso do dispositivo e quando você deve usar pilhas de dispositivo fornecidas pelo Windows.

| Para dar suporte a | Implementação |
|:---|:---|
| Dispositivos bem conhecidos, incluindo: <ul><li>Sensor</li><li>Local</li><li>Webcam</li><li>Proximidade</li><li>SMS (serviço de mensagens curtas)</li><li>Banda larga móvel</li></ul><br/> | Para muitos tipos de dispositivos bem conhecidos, você não precisa de um driver personalizado, pois o Windows inclui APIs e DDIs (interfaces de driver de dispositivo) de extensão de classe que gerenciam a comunicação entre o driver e o Windows. Os dispositivos sensor, local e dispositivo portátil do Windows (WPD) são alguns exemplos de classes de dispositivo que têm esse suporte. Se você criar um driver que usa um desses DDIs fornecidos pelo Windows para enviar e receber dados e comandos, não há necessidade de que seu aplicativo da Windows Store use a API de acesso do dispositivo para o agente de acesso ou envie códigos de controle de entrada/saída (e/s) diretamente para o driver. <br/> Quando um aplicativo da Windows Store solicita acesso a um dispositivo conhecido usando a API de Windows Runtime para sua classe de dispositivo, o Windows 8 manipulará o acesso ao dispositivo com base no tipo de dispositivo. Os aplicativos sempre terão acesso a alguns tipos conhecidos de dispositivos (como acelerômetros) que não revelam nenhuma informação de identificação pessoal. Outros tipos de dispositivos bem conhecidos devem ser declarados no manifesto do aplicativo antes que um aplicativo possa acessá-los. O usuário deve conceder permissão para que um aplicativo acesse dispositivos que revelem informações confidenciais, como dispositivos de localização, webcam e microfone, ou pode custar dinheiro ao usuário, como dispositivos de banda larga móvel. <br/> |
| Um dispositivo WPD que implementa serviços MTP.<br/> | Você pode usar o driver de classe MTP ou pode criar um driver usando a DDI WPD.<br/> O Windows 8 oferece suporte para serviços de dispositivo MTP. E um aplicativo pode usar a API do [Windows. Devices. Portable](/uwp/api/Windows.Devices.Portable) Windows Runtime, a API do dispositivo portátil Component Object Model (com) ou a automação WPD para acessar o dispositivo. Seu aplicativo não precisa usar a API de acesso do dispositivo.<br/> |
| Um dispositivo que não tem uma extensão de classe ou driver de classe fornecidos pelo Windows.<br/>  | Nesse caso, consulte os [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) para dispositivos especializados para determinar se você deve implementar o acesso de driver personalizado usando a API de acesso do dispositivo.<br/> |

## <a name="security-considerations"></a>Considerações de segurança

Os artigos a seguir fornecem orientação para escrever código C++ seguro:

- [Práticas recomendadas de segurança para C++](/cpp/security/security-best-practices-for-cpp)
- [Patterns & Practices security guidance for Applications]/Previous-Versions/MSP-n-p/ff650760 (v = PandP. 10))

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de acesso de driver personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desenvolvimento de hardware](/windows-hardware/drivers/)
