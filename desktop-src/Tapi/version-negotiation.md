---
description: Ao longo do tempo, podem existir versões diferentes para aplicativos TAPI, TAPI e provedores de serviços.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Negociação de versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922515"
---
# <a name="version-negotiation"></a>Negociação de versão

Ao longo do tempo, podem existir versões diferentes para aplicativos TAPI, TAPI e provedores de serviços. A interoperabilidade ideal de um aplicativo TAPI requer conhecimento apenas da versão da TAPI do aplicativo, mas também das versões da DLL TAPI, TAPISVR e provedor de serviços.

A falha na negociação da versão apropriada pode resultar em problemas sérios. Por exemplo, algumas estruturas muito usadas têm membros de dados adicionados de uma versão para a próxima. Se o tamanho da estrutura não corresponder ao que o aplicativo ou a TAPI espera, as consequências vão desde vazamentos de memória até a sincronização intermitente.

Para obter informações adicionais, consulte [controle de versão da TAPI](./tapi-versioning.md).

**TAPI 2. x:** Os aplicativos negociam com TAPI e TAPISVR durante o [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Os aplicativos executam a negociação de dispositivo com provedores de serviço chamando [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) para cada linha que o aplicativo pode usar.

**TAPI 3. x:** Não é necessário realizar a negociação de versão; no entanto, você pode usar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para determinar se uma interface está disponível em sua versão.

 

 
