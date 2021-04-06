---
description: A maioria das operações Get e Set lidam apenas com um componente de informações. A função phoneGetStatus retorna informações de status completas sobre um dispositivo de telefone para um aplicativo.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Status (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828329"
---
# <a name="status-telephony-api"></a>Status (API de telefonia)

A maioria das operações Get e Set lidam apenas com um componente de informações. A função [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) retorna informações de status completas sobre um dispositivo de telefone para um aplicativo.

Como mencionado anteriormente, sempre que um item de status é alterado no dispositivo de telefone, uma mensagem de [**\_ estado do telefone**](phone-state.md) é enviada para a função do aplicativo. Os parâmetros dessa mensagem incluem um identificador para o dispositivo de telefone e uma indicação do item de status que foi alterado.

Um aplicativo pode usar [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) para selecionar as alterações de status específicas para as quais deseja ser notificado. De modo correspondente, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) retorna as alterações de status para as quais o aplicativo deseja ser notificado.

 

 



