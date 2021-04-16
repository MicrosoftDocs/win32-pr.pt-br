---
description: Uma mensagem de conclusão é enviada imediatamente após uma mensagem de especificação de codificação de alteração para verificar o êxito dos processos de autenticação e troca de chaves.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Concluir mensagens no protocolo TLS 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a0f0f3e85916e66d434cb3e69b083348e40143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779363"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a><span data-ttu-id="8f911-103">Concluir mensagens no protocolo TLS 1,0</span><span class="sxs-lookup"><span data-stu-id="8f911-103">Finish Messages in the TLS 1.0 Protocol</span></span>

<span data-ttu-id="8f911-104">Uma mensagem de conclusão é enviada imediatamente após uma mensagem de especificação de codificação de alteração para verificar o êxito dos processos de autenticação e troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="8f911-104">A finish message is sent immediately after a change cipher spec message to verify the success of key exchange and authentication processes.</span></span> <span data-ttu-id="8f911-105">As mensagens de término no protocolo TLS 1,0 são calculadas usando a [*função pseudo-aleatória*](../secgloss/p-gly.md) (prf) com a [*chave mestra*](../secgloss/m-gly.md), um rótulo e uma semente como entrada.</span><span class="sxs-lookup"><span data-stu-id="8f911-105">The finish messages in the TLS 1.0 protocol are calculated using [*Pseudo-Random Function*](../secgloss/p-gly.md) (PRF) with the [*master key*](../secgloss/m-gly.md), a label, and a seed as input.</span></span> <span data-ttu-id="8f911-106">PRF produz uma saída de comprimento arbitrário.</span><span class="sxs-lookup"><span data-stu-id="8f911-106">PRF produces an output of arbitrary length.</span></span> <span data-ttu-id="8f911-107">O método a seguir é usado para gerar a saída de PRF usada em mensagens de término do TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="8f911-107">The following method is used to generate the PRF output used in TLS 1.0 finish messages.</span></span>

<span data-ttu-id="8f911-108">Um identificador de [*hash*](../secgloss/h-gly.md) de PRF é gerado usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) com o valor de **\_ ID alg** definido como CALG \_ TLS1PRF e o identificador para a chave mestra passada no parâmetro *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="8f911-108">A PRF [*hash*](../secgloss/h-gly.md) handle is generated using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with the **ALG\_ID** value set to CALG\_TLS1PRF and the handle to the master key passed in the *hKey* parameter.</span></span> <span data-ttu-id="8f911-109">Os valores de rótulo e semente são definidos no identificador de hash usando os valores HP \_ TLS1PRF \_ Label e HP \_ TLS1PRF \_ Seed, respectivamente, no parâmetro *dwParam* com a função [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) .</span><span class="sxs-lookup"><span data-stu-id="8f911-109">The label and seed values are set on the hash handle using the values HP\_TLS1PRF\_LABEL and HP\_TLS1PRF\_SEED, respectively, in the *dwParam* parameter with the [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) function.</span></span> <span data-ttu-id="8f911-110">Por fim, o mecanismo de protocolo chama a função [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) com o valor HP \_ HASHVAL no parâmetro *dwParam* para recuperar os dados de PRF a serem incluídos na mensagem de conclusão.</span><span class="sxs-lookup"><span data-stu-id="8f911-110">Finally, the protocol engine calls the function [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) with the value HP\_HASHVAL in the *dwParam* parameter to retrieve the PRF data to be included in the finish message.</span></span> <span data-ttu-id="8f911-111">Ao fazer a chamada para **CryptGetHashParam**, o mecanismo de protocolo deve especificar quantos bytes de dados o PRF produzirá.</span><span class="sxs-lookup"><span data-stu-id="8f911-111">When making the call to **CryptGetHashParam**, the protocol engine must specify how many bytes of data PRF will produce.</span></span> <span data-ttu-id="8f911-112">Isso é feito no parâmetro *pdwDataLen* e os dados resultantes são colocados no buffer apontado pelo parâmetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="8f911-112">This is done in the *pdwDataLen* parameter, and the resulting data is placed in the buffer pointed to by the *pbData* parameter.</span></span>

<span data-ttu-id="8f911-113">Este é o código-fonte típico para este mecanismo de protocolo:</span><span class="sxs-lookup"><span data-stu-id="8f911-113">The following is typical source code for this protocol engine:</span></span>


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



 

 
