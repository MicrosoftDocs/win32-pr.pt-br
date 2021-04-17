---
description: Explica como criar um CALG \_ SSL3 \_ SHAMD5 hash.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Criando um hash de CALG_SSL3_SHAMD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754501"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a>Criando um \_ \_ hash SHAMD5 do CALG SSL3

**Para criar um CALG \_ SSL3 \_ SHAMD5 hash**

1.  Usando a metodologia CryptoAPI padrão, crie um MD5 e um [](../secgloss/s-gly.md) [*hash*](../secgloss/h-gly.md) Sha dos dados de destino.
2.  Concatene os dois hashes, com o valor MD5 mais à esquerda e o valor de SHA mais à direita. Isso resulta em um valor de 36 bytes (16 bytes + 20 bytes).
3.  Obtenha um identificador para um [*objeto de hash*](../secgloss/h-gly.md) chamando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) com CALG \_ SSL3 \_ SHAMD5 passado no parâmetro *algid* .
4.  Defina o valor de hash com uma chamada para [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam). Os valores de hash concatenados são passados como um **byte** \* no parâmetro *pbData* e o valor de HASHVAL da HP \_ deve ser passado no parâmetro *dwParam* . A chamada de [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) usando o identificador retornado por [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) na etapa 3 falhará.
5.  Chame [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) para gerar a assinatura.
6.  Chame [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) para destruir o objeto de hash.

 

 
