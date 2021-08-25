---
title: Considerações de design para dispositivos personalizados
description: Este tópico descreve as considerações de design que podem ajudá-lo a determinar se o dispositivo precisa de um driver personalizado.
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 5639cf9fd51eeadc2dfb3ba84556ce6c339b6eb699e0cfa364bdee0bb03d3867
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029086"
---
# <a name="design-considerations-for-custom-devices"></a>Considerações de design para dispositivos personalizados

Este tópico descreve as considerações de design que podem ajudá-lo a determinar se o dispositivo precisa de um driver personalizado.

- [Determinando o tipo de driver a ser implementado](#determining-the-type-of-driver-to-implement)
- [Considerações sobre segurança](#security-considerations)
- [Tópicos relacionados](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>Determinando o tipo de driver a ser implementado

Esta tabela descreve quando você deve desenvolver um driver personalizado para seu dispositivo e se comunicar com ele usando o API de Acesso a Dispositivo e quando você deve usar Windows de dispositivo fornecidos.

| Para dar suporte | Implementação |
|:---|:---|
| Dispositivos conhecidos, incluindo: <ul><li>Sensor</li><li>Localização</li><li>Webcam</li><li>Proximidade</li><li>SMS (Serviço de Mensagem Curta)</li><li>Banda larga móvel</li></ul><br/> | Para muitos tipos de dispositivos conhecidos, você não precisa de um driver personalizado, pois o Windows inclui APIs e DDIs (interfaces de driver de dispositivo de extensão de classe) que gerenciam a comunicação entre o driver e o Windows. Sensor, local e Windows wpd (dispositivo portátil) são alguns exemplos de classes de dispositivo que têm esse suporte. Se você criar um driver que usa um desses DDIs fornecidos pelo Windows para enviar e receber dados e comandos, não será necessário que o aplicativo Windows Store use o API de Acesso a Dispositivo para acessar o agente ou enviar códigos de controle de E/S (entrada/saída) diretamente para o driver. <br/> Quando um aplicativo Windows Store solicita acesso a um dispositivo conhecido usando a API de Runtime do Windows para sua classe de dispositivo, Windows 8 manipulará o acesso ao dispositivo com base no tipo de dispositivo. Os aplicativos sempre terão acesso a alguns tipos conhecidos de dispositivos (como acelerômetros) que não revelam nenhuma informação de identificação pessoal. Outros tipos de dispositivos conhecidos devem ser declarados no manifesto do aplicativo antes que um aplicativo possa acessá-los. O usuário deve conceder permissão para um aplicativo acessar dispositivos que revelam informações confidenciais, como dispositivos de localização, webcam e microfone, ou pode custar o dinheiro do usuário, como dispositivos de banda larga móvel. <br/> |
| Um dispositivo WPD que implementa serviços MTP.<br/> | Você pode usar o driver de classe MTP ou pode criar um driver usando a DDI WPD.<br/> Windows 8 dá suporte para serviços de dispositivo MTP. E um aplicativo pode usar o [Windows. Devices.Portable](/uwp/api/Windows.Devices.Portable) Windows RUNtime, a API COM (Portable Device Component Object Model) ou a Automação WPD para acessar o dispositivo. Seu aplicativo não precisa usar o API de Acesso a Dispositivo.<br/> |
| Um dispositivo que não tem uma extensão de classe Windows ou driver de classe fornecido.<br/>  | Nesse caso, consulte os aplicativos de dispositivo [UWP](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) para dispositivos internos para dispositivos especializados para determinar se você deve implementar o acesso de driver personalizado usando o API de Acesso a Dispositivo.<br/> |

## <a name="security-considerations"></a>Considerações sobre segurança

Os artigos a seguir fornecem diretrizes para escrever código C++ seguro:

- [Práticas recomendadas de segurança para C++](/cpp/security/security-best-practices-for-cpp)
- [Padrões & diretrizes de segurança para aplicativos]/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de acesso de driver personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)aplicativos de dispositivo [UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de Desenvolvimento de Hardware](/windows-hardware/drivers/)
