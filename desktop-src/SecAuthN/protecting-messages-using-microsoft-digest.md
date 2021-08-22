---
description: Explica como proteger mensagens usando Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protegendo mensagens usando Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab0add351287b6c90cfe0781151c0378da56f309214b03ed12d1325a6e55d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920735"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Protegendo mensagens usando Microsoft Digest

## <a name="http-and-sasl"></a>HTTP e SASL

Como meio de detectar determinados tipos de violações de segurança, o cliente e [](../secgloss/i-gly.md) o servidor usam as funções de integridade de mensagem do SSPI [(interface](sspi.md) de provedor de suporte de segurança) [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para proteger mensagens.

Um cliente chama a [**função MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para assinar uma mensagem usando seu [*contexto de segurança*](../secgloss/s-gly.md). O servidor usa a [**função VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para verificar a origem da mensagem. Além de verificar [](../secgloss/d-gly.md) a assinatura que acompanha a mensagem, a função **VerifySignature** também verifica se a contagem de [*nonce*](../secgloss/n-gly.md) (especificada pela diretiva nc) é maior que a última contagem enviada para o nonce. Se esse não for o caso, a **função VerifySignature** retornará um código \_ de erro SEC OUT OF \_ \_ SEQUENCE.

## <a name="sasl-only"></a>Somente SASL

As [**funções EncryptMessage (Geral)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (Geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) fornecem confidencialidade para mensagens pós-autenticação trocadas entre o cliente e o servidor.

Para usar as funções de confidencialidade da mensagem, o servidor e o cliente devem ter estabelecido um contexto [*de segurança*](../secgloss/s-gly.md) com os seguintes atributos:

-   A qualidade da proteção, especificada pela diretiva qop, deve ser "auth-conf".
-   Um mecanismo de criptografia deve ter sido especificado por meio da diretiva de criptografia.

 

 
