---
description: A maioria das operações get e set lida apenas com um componente de informações. A função phoneGetStatus retorna informações de status completas sobre um dispositivo de telefone para um aplicativo.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Status (API de Telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fd9191d4b1808ca2dc5ff20ce509b58ad27a78a354aeca4ca83f8aa60dafa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861823"
---
# <a name="status-telephony-api"></a>Status (API de Telefonia)

A maioria das operações get e set lida apenas com um componente de informações. A [**função phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) retorna informações de status completas sobre um dispositivo de telefone para um aplicativo.

Conforme mencionado anteriormente, sempre que um item de status muda no dispositivo de telefone, uma [**mensagem PHONE \_ STATE**](phone-state.md) é enviada para a função de aplicativo. Os parâmetros dessa mensagem incluem um handle para o dispositivo de telefone e uma indicação do item de status que foi alterado.

Um aplicativo pode usar [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) para selecionar as alterações de status específicas para as quais deseja ser notificado. Correspondentemente, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) retorna as alterações de status para as quais o aplicativo deseja ser notificado.

 

 



