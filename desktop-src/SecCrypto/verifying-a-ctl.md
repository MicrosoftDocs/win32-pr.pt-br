---
description: Para tornar mais difícil para um interloper substituir uma CTL (lista confiável de certificados) falsa para uma existente, verifique a assinatura na CTL sempre que a CTL for usada.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Verificando uma CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502176"
---
# <a name="verifying-a-ctl"></a>Verificando uma CTL

Para tornar mais difícil para um interloper substituir uma CTL ( [*lista confiável de certificados*](../secgloss/c-gly.md) ) falsa para uma existente, verifique a assinatura na CTL sempre que a CTL for usada. Não use uma CTL que não contenha uma assinatura confiável.

**Para verificar uma assinatura de CTL**

1.  Abra o [*repositório de certificados*](../secgloss/c-gly.md) que contém a CTL desejada.
2.  Obtenha um identificador para um [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) para a CTL. Isso pode ser feito chamando qualquer uma das funções que retornam um identificador para o **\_ contexto de CTL**, como [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
3.  Chame [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passando o [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) recuperado na etapa 2 no parâmetro *hCryptMsg* , um identificador para o repositório de certificados que contém o certificado da fonte confiável para CTLs no parâmetro *rghSignerStore* e o sinalizador de \_ signatário confiável CMSG \_ \_ no parâmetro *dwFlags* . Se a função retornar **true**, a assinatura foi verificada e um ponteiro para o [**\_ contexto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) do assinante de CTL será retornado no parâmetro *ppSigner* .

 

 
