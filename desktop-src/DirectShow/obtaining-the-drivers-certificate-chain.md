---
description: Obtendo a cadeia de certificados de drivers
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Obtendo a cadeia de certificados de drivers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3f46e395550ca4bcb02396fe09126c1232f2c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825495"
---
# <a name="obtaining-the-drivers-certificate-chain"></a>Obtendo a cadeia de certificados de drivers

Para usar o protocolo COPP (certificado de proteção de saída), o aplicativo primeiro deve criar um grafo do DirectShow que inclua o filtro de renderização de mixagem de vídeo (VMR-7 ou VMR-9). O filtro de processamento de vídeo mais antigo não dá suporte a COPP. Antes de chamar qualquer método COPP, o aplicativo deve criar um grafo de reprodução de vídeo e conectar o decodificador ao PIN de entrada do filtro do VMR. Não é necessário reproduzir o arquivo de vídeo.

Depois de criar o grafo, consulte o VMR para a interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) e, em seguida, chame [**IAMCertifiedOutputProtection:: keyexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Esse método retorna um número aleatório de 128 bits digitado como um GUID, juntamente com um ponteiro para uma matriz de bytes que contém a cadeia de certificados XML do driver no formato UTF-8. O código a seguir mostra como obter a cadeia de certificados.


```C++
GUID guidRandom;
BYTE *pbCertificateChain = NULL;
DWORD cbCertificateChainLen;   // Size of the certificate chain, in bytes.
hr = pCOPP->KeyExchange(&guidRandom, &pbCertificateChain,
         &cbCertificateChainLen);
if (SUCCEEDED(hr))
{
    // TODO: Validate the certificate chain and get the driver's
    // public key. 

    // When you are done, free the buffer that contains the 
    // certificate chain.
    CoTaskMemFree(pbCertificateChain);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



