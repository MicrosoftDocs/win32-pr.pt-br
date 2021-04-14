---
title: Dispositivos (guia do desenvolvedor do Windows 7)
description: Os dispositivos são uma parte fundamental da experiência do PC, e o Windows 7 permite novas possibilidades para desenvolvedores de aplicativos que interagem com dispositivos.
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cbfa699d129fd6d8343a0645fc6ed22aa9618ee
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369155"
---
# <a name="devices-windows-7-developer-guide"></a>Dispositivos (guia do desenvolvedor do Windows 7)

Os dispositivos são uma parte fundamental da experiência do PC, e o Windows 7 permite novas possibilidades para desenvolvedores de aplicativos que interagem com dispositivos. A plataforma de experiência do dispositivo permite a associação de aplicativos e serviços a um dispositivo específico, para que os usuários possam obter o máximo benefício de seus periféricos imediatamente após a conexão. A plataforma de sensor fornece um conjunto de APIs para descoberta e comunicação com dispositivos de sensor que permitirão uma nova geração de aplicativos que estão cientes de seus ambientes. A plataforma de localização fornece novas APIs para usar dados de localização de um receptor de GPS (Global Positioning Systems) ou outros serviços que habilitam o comportamento de aplicativos específicos do local para usuários móveis. (Consulte [conceitos básicos do dispositivo – visão geral](https://www.microsoft.com/whdc/device/default.mspx).)

## <a name="device-experience-platform"></a>Plataforma de experiência do dispositivo

O Windows 7 combina software e serviços para criar novas experiências incríveis para telefones celulares, players de mídia portáteis, câmeras e impressoras. O Windows 7 torna mais fácil usar esses dispositivos diretamente da área de trabalho do Windows. Ele também fornece aos criadores de dispositivos com posicionamento proeminente na área de trabalho do Windows, com oportunidades de identidade visual e uma interface simples para apresentar a funcionalidade e os serviços aos quais o dispositivo dá suporte.

Por meio da plataforma de experiência do dispositivo, cada sessão do Windows torna-se um portal para que os clientes obtenham mais valor de seus dispositivos. A plataforma de experiência do dispositivo permite que os usuários se conectem com o fabricante do dispositivo, descubram e usem serviços relacionados e saiba mais sobre os acessórios. Como a experiência do dispositivo está conectada aos serviços Web da Microsoft, as empresas de dispositivos podem atualizar a experiência mesmo depois que os dispositivos forem enviados aos consumidores. A plataforma de experiência do dispositivo pode gerar uma experiência semelhante ao aplicativo para dispositivos com o *logotipo* do Windows, como telefones celulares.

A plataforma de experiência do dispositivo fornece aos aplicativos acesso a dispositivos como telefones celulares e media players que implementam serviços por meio do *protocolo MTP* ou do modelo de driver de [dispositivos portáteis do Windows](https://www.bing.com/search?q=Windows+Portable+Devices) .

Para habilitar a sincronização de informações pessoais entre um PC e um dispositivo, a plataforma de experiência do dispositivo hospeda uma nova plataforma de sincronização para dispositivos conectados e fornece uma interface do usuário para a seleção de aplicativos de destino para sincronização de dados, como **contatos**, **calendário** e **tarefas**. (Consulte a [experiência do dispositivo Windows](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx).)

## <a name="windows-biometric-framework"></a>Windows Biometric Framework

O Windows Biometric Framework (WBF) fornece uma API que permite que os aplicativos usem dispositivos de impressão digital para registrar, identificar e verificar identidades de usuário sem obter acesso direto a qualquer hardware ou amostra de impressão digital biométrica. Você pode usar o WBF com dispositivos de impressão digital que têm drivers WBDI (Windows biometria Device Interface). O WBF é extensível por meio de adaptadores de plug-in que gerenciam comunicações de sensor, correspondência biométrica e armazenamento de modelo. Isso garante que o WBF possa ser usado com uma ampla variedade de sensores de impressão digital. No Windows 7, os leitores de impressão digital podem usar o WBF para autenticação durante o logon do Windows e do *UAC* . (Consulte [Windows BIOMETRIC Framework API](../secbiomet/biometric-service-api-portal.md).)

 

 
