---
description: Explica como usar o suporte a mensagens SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Usando o suporte a mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755568"
---
# <a name="using-message-support"></a>Usando o suporte a mensagens

Depois que um Handshake for concluído e uma conexão segura tiver sido estabelecida, um aplicativo poderá usar as funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)e [**DecryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) para trocar dados de aplicativo assinados ou criptografados com o computador remoto.

Os exemplos que usam essas funções depois que um [*contexto de segurança*](../secgloss/s-gly.md) foi estabelecido são demonstrados nas seções a seguir:

-   [Assinando uma mensagem](signing-a-message.md)
-   [Verificando uma mensagem](verifying-a-message.md)
-   [Criptografando uma mensagem](encrypting-a-message.md)
-   [Descriptografando uma mensagem](decrypting-a-message.md)

 

 
