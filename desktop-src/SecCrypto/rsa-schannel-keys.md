---
description: Como gerar, recuperar e exportar chaves RSA/Schannel.
ms.assetid: 3069232f-d016-4973-ae39-89b0e2a03cd7
title: Chaves RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c9d23de40f32a499013928086ccb52fc1d1e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501747"
---
# <a name="rsaschannel-keys"></a>Chaves RSA/Schannel

## <a name="generating-and-retrieving-rsaschannel-keys"></a>Gerando e recuperando chaves RSA/Schannel

[*RSA*](../secgloss/r-gly.md) / As chaves [*Schannel*](../secgloss/s-gly.md) podem ser geradas chamando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . A chamada para **CryptGenKey** requer um \_ identificador de algoritmo de keyexchange passado no parâmetro *algid* .

**Para gerar um par de chaves pública/privada RSA/Schannel**

1.  Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o [provedor criptográfico Microsoft RSA/Schannel](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Chame a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para gerar as chaves. EM \_ keyexchange deve ser passado para o parâmetro *algid* e os 16 bits superiores do parâmetro *dwFlags* devem ser definidos para o tamanho de chave desejado (512 bits). Um identificador de estrutura [**HCRYPTKEY**](hcryptkey.md) é retornado no parâmetro *HKEY* .

**Para recuperar um ponteiro para chaves de usuário do RSA/Schannel geradas anteriormente**

1.  Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o [provedor criptográfico Microsoft RSA/Schannel](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Chame a função [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) , com o parâmetro *DWKEYSPEC* definido como at \_ keyexchange.

## <a name="exporting-rsaschannel-keys"></a>Exportando chaves RSA/Schannel

[*As chaves mestras*](../secgloss/m-gly.md) podem ser exportadas para estruturas de blob de chave simples. Isso deve ser implementado da mesma maneira que a exportação de [*chaves de criptografia em massa*](../secgloss/b-gly.md) [*RC4*](../secgloss/r-gly.md) ou [*padrão de criptografia de dados*](../secgloss/d-gly.md) (des) normal, conforme descrito em blob de [chave simples](https://www.bing.com/search?q=Simple+Key+BLOB). O membro **aiKeyAlg** da estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) é definido como o identificador de algoritmo da chave mestra (CALG \_ PCT1 \_ Master, CALG \_ SSL2 \_ mestre, CALG \_ SSL3 \_ Master ou CALG \_ Master TLS1 \_ ).

Se a função [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) estiver exportando uma chave mestra SSL2 e o \_ sinalizador de FALLBACK de SSL2 cript \_ estiver definido, para ajudar a evitar ataques de reversão de versão, defina os oito primeiros bytes do [*preenchimento*](../secgloss/p-gly.md) de bloco de criptografia como 0x03 em vez de dados aleatórios.

Se a constante **cript \_ DESTROYKEY** for especificada no parâmetro *dwFlags* da função [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) , o CSP destruirá a chave ou o identificador de chave depois de exportar a chave. Este sinalizador destina-se ao uso somente com [*BLOBs opacos*](../secgloss/o-gly.md).

 

 
