---
description: As mensagens são usadas para notificar a aplicação de eventos assíncronos. Todas essas mensagens são enviadas para o aplicativo por meio do mecanismo de notificação de mensagem que o aplicativo especificou em lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Mensagens TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789447"
---
# <a name="tapi-messages"></a>Mensagens TAPI

As mensagens são usadas para notificar a aplicação de eventos assíncronos. Todas essas mensagens são enviadas para o aplicativo por meio do mecanismo de notificação de mensagem que o aplicativo especificou em [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).

A mensagem sempre contém um identificador para o objeto relevante (telefone, linha ou chamada), que o aplicativo pode usar para determinar o tipo de mensagem.

Determinadas mensagens são usadas para notificar o aplicativo sobre uma alteração no status de um objeto. Essas mensagens fornecem o identificador de objeto e fornecem uma indicação de qual item de status foi alterado. O aplicativo pode chamar a função "Get status" apropriada do objeto para obter o status completo do objeto.

Quando ocorre um evento, as mensagens podem ser enviadas para zero, um ou mais aplicativos. Os aplicativos de destino para uma mensagem são determinados por vários fatores diferentes, incluindo o significado da mensagem, o privilégio do aplicativo para o objeto, se o aplicativo iniciou ou não a solicitação para a qual a mensagem é um resultado direto e o mascaramento de mensagens que foi definido pelo aplicativo. Observe os seguintes pontos sobre as mensagens:

-   As mensagens de resposta assíncronas são enviadas somente ao aplicativo que originou a solicitação e não podem ser mascaradas.
-   As mensagens que sinalizam a conclusão da geração de dígitos ou tons ou a coleta de dígitos são enviadas somente ao aplicativo que solicitou a geração de dígitos ou tons.
-   As mensagens que indicam alterações de estado de linha ou endereço são enviadas a todos os aplicativos que abriram a linha, desde que a mensagem tenha sido habilitada por meio de [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).
-   As mensagens que indicam as alterações de estado de chamada e informações de chamada são enviadas a todos os aplicativos que têm um identificador para a chamada.
-   As mensagens que sinalizam uma detecção de dígito, detecção de Tom ou detecção de tipo de mídia são enviadas para os aplicativos que solicitaram o monitoramento desse evento.

Esta seção contém as informações de referência para as seguintes mensagens TAPI:

-   [Mensagens de telefonia assistidas](assisted-telephony-messages.md)
-   [Mensagens do Call Center](call-center-messages.md)
-   [Mensagens de erro formatadas](formatted-error-messages.md)
-   [Mensagens do dispositivo de linha](line-device-messages.md)
-   [Mensagens do dispositivo de telefone](phone-device-messages.md)

 

 



