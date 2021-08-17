---
description: Explica como usar o suporte a mensagens SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Usando o suporte a mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c6a14c28cc9eb9e1b606574659412a22f375ad935ee0d7d1bdd898781c230d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785916"
---
# <a name="using-message-support"></a>Usando o suporte a mensagens

Depois que um handshake tiver sido concluído e uma conexão segura tiver sido estabelecida, um aplicativo poderá usar as funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (Geral),**](/windows/win32/api/sspi/nf-sspi-encryptmessage) [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)e [**DecryptMessage (Geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) para trocar dados de aplicativos assinados ou criptografados com o computador remoto.

Exemplos que usam essas funções depois que um [*contexto de segurança*](../secgloss/s-gly.md) é estabelecido são demonstrados nas seções a seguir:

-   [Assinando uma mensagem](signing-a-message.md)
-   [Verificando uma mensagem](verifying-a-message.md)
-   [Criptografando uma mensagem](encrypting-a-message.md)
-   [Descriptografando uma mensagem](decrypting-a-message.md)

 

 
