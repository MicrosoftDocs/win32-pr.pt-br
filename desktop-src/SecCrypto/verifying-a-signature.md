---
description: Para verificar uma assinatura, crie um objeto de hash usando CryptCreateHash. Esse objeto de hash acumula os dados a serem verificados. Os dados são então adicionados ao objeto de hash com a função CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Verificando uma assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090909"
---
# <a name="verifying-a-signature"></a>Verificando uma assinatura

Para verificar uma assinatura, crie um [*objeto de hash*](../secgloss/h-gly.md) usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Esse objeto de hash acumula os dados a serem verificados. Os dados são então adicionados ao objeto de hash com a função [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .

Depois que o último bloco de dados for adicionado ao hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) para verificar a assinatura. O endereço dos dados de assinatura, um identificador para o objeto de hash e o identificador das chaves públicas são passados para **CryptVerifySignature**.

Depois que a assinatura tiver sido verificada (ou tiver falhado na verificação), destrua o objeto de hash usando a função [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .

 

 
