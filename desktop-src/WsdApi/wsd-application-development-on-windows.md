---
description: Aprenda a usar o Microsoft Web Services em dispositivos (WSD) API (WSDAPI) para implementar dispositivos e serviços controlados pelo cliente e hosts de dispositivo em conformidade com o DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Desenvolvimento de aplicativo WSD no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d02810f55cc7ae450323543d7a0ee88f055b247fed589057e7d77710f4f86d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639346"
---
# <a name="wsd-application-development-on-windows"></a>Desenvolvimento de aplicativo WSD no Windows

A API do Microsoft Web Services on Devices (WSDAPI) dá suporte à implementação de dispositivos e serviços controlados pelo cliente e aos hosts de dispositivo em conformidade com o [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). O WSDAPI pode ser usado para o desenvolvimento de implementações de cliente e de servidor (dispositivo).

Com muita frequência, o código WSDAPI para esses aplicativos é gerado usando [WsdCodeGen](web-services-for-devices-code-generator.md). Algumas funções e métodos WSDAPI devem ser chamados apenas pelo código gerado. A documentação de referência de API indica quando uma função ou método deve ser usado ou implementado somente pelo código gerado.

o SDK do Windows inclui alguns arquivos WSDL de exemplo, arquivos de configuração WsdCodeGen e código gerado. Para obter mais informações, consulte [exemplos de WSDAPI](wsdapi-samples.md).

Se você quiser enumerar dispositivos usando o protocolo WSD e consultar metadados de dispositivo WSD, poderá usar a API de [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) em vez disso.

se você quiser implementar um dispositivo wsd que não execute Windows, consulte desenvolvimento de [dispositivo wsd](wsd-device-development.md).
