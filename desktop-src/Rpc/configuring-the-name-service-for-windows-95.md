---
title: configurando o serviço de nome para o Windows 95
description: Windows 95 não usa o Microsoft Locator.
ms.assetid: 0903681c-9cbf-4c5c-8637-be7f6501cd14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d50f1dc3d54c3b1890b2f0b4cfc1f7285044fd895bbfb692cba1db909a2bd26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931513"
---
# <a name="configuring-the-name-service-for-windows-95"></a>configurando o serviço de nome para o Windows 95

Windows 95 não usa o Microsoft Locator. para usar um serviço de nome em um aplicativo Windows 95, o computador com Windows 95 deve:

-   faça parte de um grupo de trabalho ou domínio que inclua um computador executando o Windows 2000 ou Windows NT para servir como um provedor de serviços de nome de proxy.
-   Estar conectado a um computador host que executa o daemon de NSI (nsid), que serve como um gateway para o serviço de diretório de células do DCE do Digital Equipment Corporation.

 

 




