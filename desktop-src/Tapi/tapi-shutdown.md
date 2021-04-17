---
description: O desligamento adequado das sessões de comunicação e de um aplicativo inteiro é necessário para impedir que os recursos permaneçam ligados em chamadas ou aplicativos que não precisam mais deles.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Desligamento TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782898"
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



 

 

 
