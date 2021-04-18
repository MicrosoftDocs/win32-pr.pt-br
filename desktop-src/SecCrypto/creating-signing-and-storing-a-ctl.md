---
description: Crie uma CTL (lista de certificados confiáveis) assinada e salve-a em um repositório de certificados.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Criando, assinando e armazenando uma CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760203"
---
# <a name="creating-signing-and-storing-a-ctl"></a>Criando, assinando e armazenando uma CTL

Os procedimentos a seguir criam uma CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ) assinada e salvam-a em um [*repositório de certificados*](../secgloss/c-gly.md).

**Para criar e assinar uma CTL**

1.  Crie uma matriz de itens a serem armazenados na [*CTL*](../secgloss/c-gly.md). No caso de certificados confiáveis, esses devem ser os hashes SHA1 ou MD5 dos certificados confiáveis.
2.  Inicialize uma estrutura de [**\_ informações de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) que inclua a matriz de itens que acabou de ser criada.
3.  Inicializar uma estrutura de [**\_ \_ \_ informações de codificação assinada CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .
4.  Chame [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl). Essa chamada de função retorna um ponteiro para uma CTL assinada e codificada (no \# formato PKCS 7) que contém a lista de itens criados na etapa 1.

**Para adicionar uma CTL a um repositório de certificados**

1.  Obtenha um ponteiro para uma CTL assinada e codificada.
2.  Abra o repositório de certificados de destino com uma chamada para [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
3.  Chame [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).

 

 
