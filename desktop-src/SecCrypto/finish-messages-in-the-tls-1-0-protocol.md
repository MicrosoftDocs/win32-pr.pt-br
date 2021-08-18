---
description: Uma mensagem de conclusão é enviada imediatamente após uma mensagem de especificação de codificação de alteração para verificar o êxito dos processos de autenticação e troca de chaves.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Concluir mensagens no protocolo TLS 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e9af7502f0865661e2ed0f6a80059cb822395002ccaf035373dc3db322adac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006974"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a>Concluir mensagens no protocolo TLS 1,0

Uma mensagem de conclusão é enviada imediatamente após uma mensagem de especificação de codificação de alteração para verificar o êxito dos processos de autenticação e troca de chaves. As mensagens de término no protocolo TLS 1,0 são calculadas usando a [*função pseudo-aleatória*](../secgloss/p-gly.md) (prf) com a [*chave mestra*](../secgloss/m-gly.md), um rótulo e uma semente como entrada. PRF produz uma saída de comprimento arbitrário. O método a seguir é usado para gerar a saída de PRF usada em mensagens de término do TLS 1,0.

Um identificador de [*hash*](../secgloss/h-gly.md) de PRF é gerado usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) com o valor de **\_ ID alg** definido como CALG \_ TLS1PRF e o identificador para a chave mestra passada no parâmetro *HKEY* . Os valores de rótulo e semente são definidos no identificador de hash usando os valores HP \_ TLS1PRF \_ Label e HP \_ TLS1PRF \_ Seed, respectivamente, no parâmetro *dwParam* com a função [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) . Por fim, o mecanismo de protocolo chama a função [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) com o valor HP \_ HASHVAL no parâmetro *dwParam* para recuperar os dados de PRF a serem incluídos na mensagem de conclusão. Ao fazer a chamada para **CryptGetHashParam**, o mecanismo de protocolo deve especificar quantos bytes de dados o PRF produzirá. Isso é feito no parâmetro *pdwDataLen* e os dados resultantes são colocados no buffer apontado pelo parâmetro *pbData* .

Este é o código-fonte típico para este mecanismo de protocolo:


```C++
CRYPT_DATA_BLOB Data;
HCRYPTHASH hFinishHash;
BYTE rgbFinishPRF[12];
BYTE rgbCliHashOfHandshakes[36];

//------------------------------------------------------------
// get client finish message

CryptCreateHash(
         hProv, 
         CALG_TLS1PRF, 
         hMasterKey, 
         0, 
         &hFinishHash);

Data.pbData = (BYTE*)"client finished";
Data.cbData = 15;
CryptSetHashParam(
         hFinishHash, 
         HP_TLS1PRF_LABEL, 
         (BYTE*)&Data, 
         0);

Data.pbData = rgbCliHashOfHandshakes;
Data.cbData = sizeof(rgbCliHashOfHandshakes);
CryptSetHashParam(
          hFinishHash, 
          HP_TLS1PRF_SEED, 
          (BYTE*)&Data, 
          0);

cbFinishPRF = sizeof(rgbFinishPRF);
CryptGetHashParam(
          hFinishHash, 
          HP_HASHVAL, 
          rgbFinishPRF, 
          &cbFinishPRF, 
          0);

CryptDestroyHash(hFinishHash);
```



 

 
