---
description: Alguns protocolos exigem várias mensagens de autenticação.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Continuação do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827765"
---
# <a name="client-continuation"></a>Continuação do cliente

Alguns protocolos exigem várias mensagens de autenticação. Nesse caso, o cliente analisa a resposta do servidor e chama [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) novamente usando o status de continuação da chamada anterior. O cliente verifica o status de retorno dessa chamada e pode ser necessário para continuar para os segmentos adicionais. Ele usa as informações em *pOutput* para construir uma mensagem e a envia para o servidor.

 

 
