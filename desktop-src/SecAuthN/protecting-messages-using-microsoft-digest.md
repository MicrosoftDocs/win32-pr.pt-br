---
description: Explica como proteger mensagens usando Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protegendo mensagens usando Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747301"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Protegendo mensagens usando Microsoft Digest

## <a name="http-and-sasl"></a>HTTP e SASL

Como um meio de detectar determinados tipos de violações de segurança, o cliente e o servidor usam as funções de [*integridade*](../secgloss/i-gly.md) de mensagem do SSPI ( [Security Support Provider interface](sspi.md) ) [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para proteger as mensagens.

Um cliente chama a função [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para assinar uma mensagem usando seu [*contexto de segurança*](../secgloss/s-gly.md). O servidor usa a função [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para verificar a origem da mensagem. Além de verificar a [*assinatura*](../secgloss/d-gly.md) que acompanha a mensagem, a função **VerifySignature** também verifica se a contagem de [*nonce*](../secgloss/n-gly.md) (especificada pela diretiva NC) é uma maior que a última contagem enviada para o nonce. Se esse não for o caso, a função **VerifySignature** retornará uma SEC \_ fora \_ do \_ código de erro de sequência.

## <a name="sasl-only"></a>SASL somente

As funções [**EncryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) fornecem confidencialidade para mensagens de pós-autenticação trocadas entre o cliente e o servidor.

Para usar as funções de confidencialidade da mensagem, o servidor e o cliente devem ter estabelecido um [*contexto de segurança*](../secgloss/s-gly.md) com os seguintes atributos:

-   A qualidade de proteção, especificada pela diretiva QoP, deve ser "auth-conf".
-   Um mecanismo de criptografia deve ter sido especificado por meio da diretiva de codificação.

 

 
