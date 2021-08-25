---
description: Crie uma CTL (lista de confiança de certificado) assinada e salve-a em um armazenamento de certificados.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Criando, assinando e armazenar uma CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f9aac8c75f7c112a09c62bb52d6e554aee7703e7f3e02c101545de5c5196db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876556"
---
# <a name="creating-signing-and-storing-a-ctl"></a>Criando, assinando e armazenar uma CTL

Os procedimentos a seguir criam uma CTL [*(lista*](../secgloss/c-gly.md) de confiança de certificado) assinada e a salvam em um [*armazenamento de certificados.*](../secgloss/c-gly.md)

**Para criar e assinar uma CTL**

1.  Crie uma matriz de itens a serem armazenados na [*CTL.*](../secgloss/c-gly.md) No caso de certificados confiáveis, isso deve ser os hashes SHA1 ou MD5 dos certificados confiáveis.
2.  Inicialize uma [**estrutura CTL \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) que inclui a matriz de itens que acabou de ser criada.
3.  Inicializar uma estrutura [**DE INFORMAÇÕES DE \_ \_ CODIFICAÇÃO ASSINADA \_ DO CMSG.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)
4.  Chame [**CryptMsgEncodeAndSignCTL.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl) Essa chamada de função retorna um ponteiro para uma CTL codificada assinada (no formato PKCS 7) que contém a lista de itens criados \# na etapa 1.

**Para adicionar uma CTL a um armazenamento de certificados**

1.  Obter um ponteiro para uma CTL assinada e codificada.
2.  Abra o repositório de certificados de destino com uma [**chamada para CertOpenStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)
3.  Chame [**CertAddEncodedCTLToStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

 

 
