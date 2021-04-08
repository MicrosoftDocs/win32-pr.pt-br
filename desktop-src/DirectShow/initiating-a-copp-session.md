---
description: Iniciando uma sessão COPP
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: Iniciando uma sessão COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d64ef848874aee95d3f928a5b8bb637323a92a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087794"
---
# <a name="initiating-a-copp-session"></a><span data-ttu-id="96735-103">Iniciando uma sessão COPP</span><span class="sxs-lookup"><span data-stu-id="96735-103">Initiating a COPP Session</span></span>

<span data-ttu-id="96735-104">Para iniciar uma sessão de COPP (protocolo de proteção de saída) certificada, você deve preparar uma *assinatura*, que é uma matriz que contém a concatenação dos seguintes números:</span><span class="sxs-lookup"><span data-stu-id="96735-104">To initiate a Certified Output Protection Protocol (COPP) session, you must prepare a *signature*, which is an array that contains the concatenation of the following numbers:</span></span>

-   <span data-ttu-id="96735-105">O número aleatório de 128 bits retornado pelo driver.</span><span class="sxs-lookup"><span data-stu-id="96735-105">The 128-bit random number returned by the driver.</span></span> <span data-ttu-id="96735-106">(Esse valor é mostrado como *guidRandom* em [obter a cadeia de certificados do driver](obtaining-the-drivers-certificate-chain.md).)</span><span class="sxs-lookup"><span data-stu-id="96735-106">(This value is shown as *guidRandom* in [Obtaining the Driver's Certificate Chain](obtaining-the-drivers-certificate-chain.md).)</span></span>
-   <span data-ttu-id="96735-107">Uma chave AES simétrica de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="96735-107">A 128-bit symmetric AES key.</span></span>
-   <span data-ttu-id="96735-108">Um número de sequência inicial de 32 bits para solicitações de status.</span><span class="sxs-lookup"><span data-stu-id="96735-108">A 32-bit starting sequence number for status requests.</span></span>
-   <span data-ttu-id="96735-109">Um número de sequência inicial de 32 bits para comandos de COPP.</span><span class="sxs-lookup"><span data-stu-id="96735-109">A 32-bit starting sequence number for COPP commands.</span></span>

<span data-ttu-id="96735-110">Gere uma chave AES simétrica da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="96735-110">Generate a symmetric AES key as follows:</span></span>


```C++
DWORD dwFlag = 0x80;         // Bit length: 128-bit AES.
dwFlag <<= 16;               // Move this value to the upper 16 bits.
dwFlag |= CRYPT_EXPORTABLE;  // We want to export the key.
CryptGenKey(
    hCSP,           // Handle to the CSP.
    CALG_AES_128,   // Use 128-bit AES block encryption algorithm.
    dwFlag,
    &m_hAESKey      // Receives a handle to the AES key.
);
```



<span data-ttu-id="96735-111">A função **CryptGenKey** cria a chave simétrica, mas a chave ainda é mantida no CSP.</span><span class="sxs-lookup"><span data-stu-id="96735-111">The **CryptGenKey** function creates the symmetric key, but the key is still held in the CSP.</span></span> <span data-ttu-id="96735-112">Para exportar a chave para uma matriz de bytes, use a função **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="96735-112">To export the key into a byte array, use the **CryptExportKey** function.</span></span> <span data-ttu-id="96735-113">Esse é o motivo para usar o \_ sinalizador EXportável incompreensíveI ao chamar **CryptGenKey**.</span><span class="sxs-lookup"><span data-stu-id="96735-113">This is the reason for using the CRYPT\_EXPORTABLE flag when calling **CryptGenKey**.</span></span> <span data-ttu-id="96735-114">O código a seguir exporta a chave e a copia para o</span><span class="sxs-lookup"><span data-stu-id="96735-114">The following code exports the key and copies it into the</span></span>


```
pData
```



<span data-ttu-id="96735-115">matriz.</span><span class="sxs-lookup"><span data-stu-id="96735-115">array.</span></span>


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



<span data-ttu-id="96735-116">Os dados retornados em</span><span class="sxs-lookup"><span data-stu-id="96735-116">The data returned in</span></span>


```
pData
```



<span data-ttu-id="96735-117">tem o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="96735-117">has the following layout:</span></span>


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



<span data-ttu-id="96735-118">No entanto, nenhuma estrutura correspondente a esse layout é definida nos cabeçalhos do CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="96735-118">However, no structure that matches this layout is defined in the CryptoAPI headers.</span></span> <span data-ttu-id="96735-119">Você pode definir uma ou qualquer aritmética de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="96735-119">You can either define one or do some pointer arithmetic.</span></span> <span data-ttu-id="96735-120">Por exemplo, para verificar o tamanho da chave:</span><span class="sxs-lookup"><span data-stu-id="96735-120">For example, to verify the size of the key:</span></span>


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



<span data-ttu-id="96735-121">Para obter o ponteiro para a chave em si:</span><span class="sxs-lookup"><span data-stu-id="96735-121">To get the pointer to the key itself:</span></span>


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



<span data-ttu-id="96735-122">Em seguida, gere um número aleatório de 32 bits para usar como a sequência inicial para solicitações de status COPP.</span><span class="sxs-lookup"><span data-stu-id="96735-122">Next, generate a 32-bit random number to use as the starting sequence for COPP status requests.</span></span> <span data-ttu-id="96735-123">A maneira recomendada para criar um número aleatório é chamar a função **CryptGenRandom** .</span><span class="sxs-lookup"><span data-stu-id="96735-123">The recommended way to create a random number is to call the **CryptGenRandom** function.</span></span> <span data-ttu-id="96735-124">Não use a função **Rand** na biblioteca de tempo de execução do C, pois ela não é realmente aleatória.</span><span class="sxs-lookup"><span data-stu-id="96735-124">Do not use the **rand** function in the C run-time library, because it is not truly random.</span></span> <span data-ttu-id="96735-125">Gere um segundo número aleatório de 32 bits para usar como a sequência inicial para comandos COPP.</span><span class="sxs-lookup"><span data-stu-id="96735-125">Generate a second 32-bit random number to use as the starting sequence for COPP commands.</span></span>


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



<span data-ttu-id="96735-126">Agora você pode preparar a assinatura COPP.</span><span class="sxs-lookup"><span data-stu-id="96735-126">Now you can prepare the COPP signature.</span></span> <span data-ttu-id="96735-127">Essa é uma matriz de 256 bytes, definida como a estrutura [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) .</span><span class="sxs-lookup"><span data-stu-id="96735-127">This is a 256-byte array, defined as the [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) structure.</span></span> <span data-ttu-id="96735-128">Inicialize o conteúdo da matriz para zero.</span><span class="sxs-lookup"><span data-stu-id="96735-128">Initialize the contents of the array to zero.</span></span> <span data-ttu-id="96735-129">Em seguida, copie os quatro números na matriz — o número aleatório do driver, a chave AES, o número de sequência de status e o número de sequência de comando, nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="96735-129">Then copy the four numbers into the array—the driver's random number, the AES key, the status sequence number, and the command sequence number, in that order.</span></span> <span data-ttu-id="96735-130">Por fim, troque a ordem de bytes de toda a matriz.</span><span class="sxs-lookup"><span data-stu-id="96735-130">Finally, swap the byte order of the entire array.</span></span>

<span data-ttu-id="96735-131">De acordo com a documentação do **CryptEncrypt**:</span><span class="sxs-lookup"><span data-stu-id="96735-131">According to the documentation for **CryptEncrypt**:</span></span>

<dl> <span data-ttu-id="96735-132">"O comprimento dos dados de texto sem formatação que podem ser criptografados com uma chamada para **CryptEncrypt** com uma chave RSA é o comprimento do módulo de chave menos onze bytes.</span><span class="sxs-lookup"><span data-stu-id="96735-132">"The length of plaintext data that can be encrypted with a call to **CryptEncrypt** with an RSA key is the length of the key modulus minus eleven bytes.</span></span> <span data-ttu-id="96735-133">O mínimo de onze bytes é escolhido para o \# preenchimento PKCS 1. "</span><span class="sxs-lookup"><span data-stu-id="96735-133">The eleven bytes is the chosen minimum for PKCS \#1 padding."</span></span>  
</dl>

<span data-ttu-id="96735-134">Nesse caso, o módulo tem 256 bytes, portanto, o comprimento máximo da mensagem é de 245 bytes (256 – 11).</span><span class="sxs-lookup"><span data-stu-id="96735-134">In this case, the modulus is 256 bytes, so the maximum message length is 245 bytes (256 – 11).</span></span> <span data-ttu-id="96735-135">A estrutura **AMCOPPSignature** é de 256 bytes, mas os dados significativos na assinatura são apenas 40 bytes.</span><span class="sxs-lookup"><span data-stu-id="96735-135">The **AMCOPPSignature** structure is 256 bytes, but the meaningful data in the signature is only 40 bytes.</span></span> <span data-ttu-id="96735-136">O código a seguir criptografa a assinatura e fornece o resultado em</span><span class="sxs-lookup"><span data-stu-id="96735-136">The following code encrypts the signature and provides the result in</span></span>


```
CoppSig
```



<span data-ttu-id="96735-137">.</span><span class="sxs-lookup"><span data-stu-id="96735-137">.</span></span>


```C++
AMCOPPSignature CoppSig;
ZeroMemory(&CoppSig, sizeof(CoppSig));
// Copy the signature data into CoppSig. (Not shown.)

// Encrypt the signature:
const DWORD RSA_PADDING = 11;    // 11-byte padding.
DWORD cbDataOut = sizeof(AMCOPPSignature);
DWORD cbDataIn = cbDataOut - RSA_PADDING;
CryptEncrypt(
    hRSAKey, 
    NULL,     // No hash object.
    TRUE,     // Final block to encrypt.
    0,        // Reserved.
    &CoppSig, // COPP signature.
    &cbDataOut, 
    cbDataIn
);
```



<span data-ttu-id="96735-138">Agora passe a matriz criptografada para [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span><span class="sxs-lookup"><span data-stu-id="96735-138">Now pass the encrypted array to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span></span>


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



<span data-ttu-id="96735-139">Se esse método tiver sucesso, você estará pronto para enviar comandos COPP e solicitações de status para o driver.</span><span class="sxs-lookup"><span data-stu-id="96735-139">If this method succeeds, you are ready to send COPP commands and status requests to the driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96735-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96735-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96735-141">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="96735-141">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



