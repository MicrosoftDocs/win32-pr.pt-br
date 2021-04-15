---
description: Estas etapas verificam a assinatura de dados assinados.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Verificando uma mensagem assinada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768426"
---
# <a name="verifying-a-signed-message"></a>Verificando uma mensagem assinada

Estas etapas verificam a assinatura de dados assinados. A ilustração a seguir descreve as tarefas individuais que devem ser realizadas, conforme mostrado na lista que a segue.

![Verificando uma mensagem assinada](images/verifmsg.png)

**Para verificar a assinatura de uma mensagem assinada**

1.  Obtenha um ponteiro para a mensagem assinada.
2.  Abra um [*repositório de certificados*](../secgloss/c-gly.md).
3.  Usando a ID de signatário contida na mensagem, obtenha o certificado do remetente e obtenha um identificador para sua [*chave pública*](../secgloss/p-gly.md).

    Como alternativa às etapas 2 e 3, você pode usar o certificado contido na mensagem para recuperar a chave pública do signatário.

4.  Usando a chave pública do signatário, descriptografe a assinatura digital, produzindo o resumo original dos dados na mensagem.
5.  Usando o algoritmo de hash contido na mensagem, gere o [*hash*](../secgloss/h-gly.md) dos dados contidos na mensagem, produzindo um novo Resumo.
6.  Compare o resumo recuperado da mensagem com o novo Resumo recém-criado.
7.  Se os dois resumos forem correspondentes, a assinatura será verificada. Isso significa que a [*chave privada*](../secgloss/p-gly.md) usada para assinar os dados corresponde à chave pública usada apenas para descriptografar a assinatura e que os dados não foram alterados desde que os dados foram assinados.

    Se os dois resumos não corresponderem, a assinatura não será verificada e as chaves privada/pública não corresponderão, ou os dados foram alterados desde que os dados foram assinados, ou ambos.

Uma única função, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), pode ser usada para verificar uma assinatura, conforme mostrado no procedimento a seguir.

**Para verificar uma mensagem assinada**

1.  Obtenha um ponteiro para a mensagem assinada.
2.  Obtenha o tamanho da mensagem assinada.
3.  Obtenha um identificador em um provedor criptográfico.
4.  Inicialize a estrutura da [**\_ \_ mensagem \_ de verificação cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) .
5.  Chame [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) para verificar a assinatura.

O código que implementa esse procedimento está incluído no [programa de exemplo C: assinando uma mensagem e verificando uma assinatura de mensagem](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
