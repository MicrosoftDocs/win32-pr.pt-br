---
description: O desligamento adequado das sessões de comunicação e de um aplicativo inteiro é necessário para impedir que os recursos permaneçam ligados em chamadas ou aplicativos que não precisam mais deles.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Desligamento TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88303d2475a2ce0a21478575483c0fd93e44e96b71efa83790b7973343d6d9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080435"
---
# <a name="tapi-shutdown"></a>Desligamento TAPI

O desligamento adequado das sessões de comunicação e de um aplicativo inteiro é necessário para impedir que os recursos permaneçam ligados em chamadas ou aplicativos que não precisam mais deles.

A TAPI fornece uma série de funções e métodos para ajudar no processo. Obviamente, o aplicativo também deve assumir a responsabilidade de liberar corretamente a memória alocada, seja na forma de estruturas de dados ou referências COM.



| Funções TAPI 2. x                                                            | Descrição                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | Cancela o registro do aplicativo como um manipulador para chamadas telefônicas assistidas. |
| [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | Desconecta o aplicativo como um gerente para chamadas na linha especificada.  |
| [**lineShutdown**](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | Desliga o uso do aplicativo da abstração de linha.            |



 



| Interfaces ou métodos TAPI 3. x                                            | Descrição                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ITTAPI::UnregisterNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | Remove todos os registros de notificação de eventos executados pelo aplicativo. |
| [**ITTAPI:: Shutdown**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | Desconecta o aplicativo como um Gerenciador de chamadas.                             |



 

 

 
