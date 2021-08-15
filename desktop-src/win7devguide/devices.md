---
title: dispositivos (guia do desenvolvedor Windows 7)
description: os dispositivos são uma parte fundamental da experiência do PC e o Windows 7 permite novas possibilidades para os desenvolvedores de aplicativos que interagem com dispositivos.
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775389f1a3548e2e94b8b2c25f9b46560cef5fc61a5e486f5dff28871da9f9e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086729"
---
# <a name="devices-windows-7-developer-guide"></a>dispositivos (guia do desenvolvedor Windows 7)

os dispositivos são uma parte fundamental da experiência do PC e o Windows 7 permite novas possibilidades para os desenvolvedores de aplicativos que interagem com dispositivos. A plataforma de experiência do dispositivo permite a associação de aplicativos e serviços a um dispositivo específico, para que os usuários possam obter o máximo benefício de seus periféricos imediatamente após a conexão. A plataforma de sensor fornece um conjunto de APIs para descoberta e comunicação com dispositivos de sensor que permitirão uma nova geração de aplicativos que estão cientes de seus ambientes. A plataforma de localização fornece novas APIs para usar dados de localização de um receptor de GPS (Global Positioning Systems) ou outros serviços que habilitam o comportamento de aplicativos específicos do local para usuários móveis. (Consulte [conceitos básicos do dispositivo – visão geral](https://www.microsoft.com/whdc/device/default.mspx).)

## <a name="device-experience-platform"></a>Plataforma de experiência do dispositivo

o Windows 7 combina software e serviços para criar novas experiências incríveis para telefones celulares, players de mídia portáteis, câmeras e impressoras. Windows 7 facilita o uso desses dispositivos diretamente da área de trabalho do Windows. ele também fornece aos criadores de dispositivos com posicionamento proeminente na área de trabalho Windows, com oportunidades de identidade visual e uma interface simples para apresentar a funcionalidade e os serviços aos quais o dispositivo dá suporte.

por meio da plataforma de experiência do dispositivo, cada sessão de Windows se torna um portal para que os clientes obtenham mais valor de seus dispositivos. A plataforma de experiência do dispositivo permite que os usuários se conectem com o fabricante do dispositivo, descubram e usem serviços relacionados e saiba mais sobre os acessórios. Como a experiência do dispositivo está conectada aos serviços Web da Microsoft, as empresas de dispositivos podem atualizar a experiência mesmo depois que os dispositivos forem enviados aos consumidores. a plataforma de experiência do dispositivo pode gerar uma experiência semelhante ao aplicativo para dispositivos Windows *logotipos* , como telefones celulares.

a plataforma de experiência do dispositivo fornece aos aplicativos acesso a dispositivos como celulares e media players que implementam serviços por meio do *MTP (protocolo de transferência de mídia)* ou o modelo de driver de [dispositivos portáteis Windows](https://www.bing.com/search?q=Windows+Portable+Devices) .

Para habilitar a sincronização de informações pessoais entre um PC e um dispositivo, a plataforma de experiência do dispositivo hospeda uma nova plataforma de sincronização para dispositivos conectados e fornece uma interface do usuário para a seleção de aplicativos de destino para sincronização de dados, como **contatos**, **calendário** e **tarefas**. (consulte [Windows experiência do dispositivo](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx).)

## <a name="windows-biometric-framework"></a>Windows Biometric Framework

o Windows Biometric Framework (WBF) fornece uma API que permite que os aplicativos usem dispositivos de impressão digital para registrar, identificar e verificar identidades de usuário sem obter acesso direto a qualquer hardware ou amostra de impressão digital biométrica. você pode usar o WBF com dispositivos de impressão digital que Windows têm drivers de WBDI (biométrica dispositivo Interface). O WBF é extensível por meio de adaptadores de plug-in que gerenciam comunicações de sensor, correspondência biométrica e armazenamento de modelo. Isso garante que o WBF possa ser usado com uma ampla variedade de sensores de impressão digital. no Windows 7, os leitores de impressão digital podem usar o WBF para autenticação durante o *UAC* e o logon do Windows. (consulte [Windows Biometric Framework API](../secbiomet/biometric-service-api-portal.md).)

 

 
