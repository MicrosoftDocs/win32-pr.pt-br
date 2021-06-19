---
description: Aprenda a usar o Microsoft Web Services em dispositivos (WSD) API (WSDAPI) para implementar dispositivos e serviços controlados pelo cliente e hosts de dispositivo em conformidade com o DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Desenvolvimento de aplicativos WSD no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405779"
---
# <a name="wsd-application-development-on-windows"></a>Desenvolvimento de aplicativos WSD no Windows

A API do Microsoft Web Services on Devices (WSDAPI) dá suporte à implementação de dispositivos e serviços controlados pelo cliente e aos hosts de dispositivo em conformidade com o [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). O WSDAPI pode ser usado para o desenvolvimento de implementações de cliente e de servidor (dispositivo).

Com muita frequência, o código WSDAPI para esses aplicativos é gerado usando [WsdCodeGen](web-services-for-devices-code-generator.md). Algumas funções e métodos WSDAPI devem ser chamados apenas pelo código gerado. A documentação de referência de API indica quando uma função ou método deve ser usado ou implementado somente pelo código gerado.

O SDK do Windows inclui alguns arquivos WSDL de exemplo, arquivos de configuração WsdCodeGen e código gerado. Para obter mais informações, consulte [exemplos de WSDAPI](wsdapi-samples.md).

Se você quiser enumerar dispositivos usando o protocolo WSD e consultar metadados de dispositivo WSD, poderá usar a API de [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) em vez disso.

Se você quiser implementar um dispositivo WSD que não executa o Windows, consulte [desenvolvimento de dispositivo WSD](wsd-device-development.md).
