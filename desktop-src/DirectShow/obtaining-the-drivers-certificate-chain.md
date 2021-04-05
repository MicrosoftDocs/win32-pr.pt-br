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
# <a name="obtaining-the-drivers-certificate-chain"></a><span data-ttu-id="232bf-103">Obtendo a cadeia de certificados de drivers</span><span class="sxs-lookup"><span data-stu-id="232bf-103">Obtaining the Drivers Certificate Chain</span></span>

<span data-ttu-id="232bf-104">Para usar o protocolo COPP (certificado de proteção de saída), o aplicativo primeiro deve criar um grafo do DirectShow que inclua o filtro de renderização de mixagem de vídeo (VMR-7 ou VMR-9).</span><span class="sxs-lookup"><span data-stu-id="232bf-104">To use Certified Output Protection Protocol (COPP), the application first must build a DirectShow graph that includes the Video Mixing Render filter (VMR-7 or VMR-9).</span></span> <span data-ttu-id="232bf-105">O filtro de processamento de vídeo mais antigo não dá suporte a COPP.</span><span class="sxs-lookup"><span data-stu-id="232bf-105">The older Video Renderer filter does not support COPP.</span></span> <span data-ttu-id="232bf-106">Antes de chamar qualquer método COPP, o aplicativo deve criar um grafo de reprodução de vídeo e conectar o decodificador ao PIN de entrada do filtro do VMR.</span><span class="sxs-lookup"><span data-stu-id="232bf-106">Before calling any COPP methods, the application must build a video playback graph and connect the decoder to the VMR filter's input pin.</span></span> <span data-ttu-id="232bf-107">Não é necessário reproduzir o arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="232bf-107">It is not necessary to play the video file.</span></span>

<span data-ttu-id="232bf-108">Depois de criar o grafo, consulte o VMR para a interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) e, em seguida, chame [**IAMCertifiedOutputProtection:: keyexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="232bf-108">After building the graph, query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface, and then call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="232bf-109">Esse método retorna um número aleatório de 128 bits digitado como um GUID, juntamente com um ponteiro para uma matriz de bytes que contém a cadeia de certificados XML do driver no formato UTF-8.</span><span class="sxs-lookup"><span data-stu-id="232bf-109">This method returns a 128-bit random number typed as a GUID, along with a pointer to a byte array that contains the driver's XML certificate chain in UTF-8 format.</span></span> <span data-ttu-id="232bf-110">O código a seguir mostra como obter a cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="232bf-110">The following code shows how to get the certificate chain.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="232bf-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="232bf-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="232bf-112">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="232bf-112">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



