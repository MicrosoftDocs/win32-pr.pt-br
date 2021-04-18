---
description: As funções de telefonia estendidas são listadas por categoria nas tabelas a seguir.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Referência de serviços de telefonia estendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766979"
---
# <a name="extended-telephony-services-reference"></a>Referência de serviços de telefonia estendida

As funções de telefonia estendidas são listadas por categoria nas tabelas a seguir.

## <a name="extended-telephony-functions-for-line-devices"></a>Funções de telefonia estendidas para dispositivos de linha



| Função                                                   | Descrição                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | Permite que um aplicativo negocie uma versão de extensão para usar com o dispositivo de linha especificado. Assíncrono. |
| [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | Dá aos provedores de serviços acesso a recursos específicos do dispositivo não oferecidos por outras funções TAPI. Synchronous. |
| [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | Envia recursos de comutador específicos do dispositivo para o comutador. Assíncrono.                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a>Funções de telefonia estendidas para dispositivos de telefone



| Função                                                     | Descrição                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | Função de escape específica do dispositivo para permitir extensões dependentes do fornecedor. Assíncrono.                          |
| [**PhoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Permite que um aplicativo negocie uma versão de extensão para usar com o dispositivo de telefone especificado. Synchronous. |



 

 

 



