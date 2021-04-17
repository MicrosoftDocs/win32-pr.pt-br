---
description: Listas de Revogação de Certificados
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Listas de Revogação de Certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105769220"
---
# <a name="certificate-revocation-lists"></a><span data-ttu-id="d932f-103">Listas de Revogação de Certificados</span><span class="sxs-lookup"><span data-stu-id="d932f-103">Certificate Revocation Lists</span></span>

<span data-ttu-id="d932f-104">Este tópico descreve como examinar a CRL (lista de certificados revogados) para drivers revogados ao usar o protocolo COPP (certificado de proteção de saída).</span><span class="sxs-lookup"><span data-stu-id="d932f-104">This topic describes how to examine the certificate revocation list (CRL) for revoked drivers when using Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="d932f-105">A CRL contém resumos de certificados revogados e pode ser fornecida e assinada somente pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d932f-105">The CRL contains digests of revoked certificates and can be provided and signed only by Microsoft.</span></span> <span data-ttu-id="d932f-106">A CRL é distribuída por meio de licenças do DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="d932f-106">The CRL is distributed through digital rights management (DRM) licenses.</span></span> <span data-ttu-id="d932f-107">A CRL pode revogar qualquer certificado na cadeia de certificados do driver.</span><span class="sxs-lookup"><span data-stu-id="d932f-107">The CRL can revoke any certificate in the driver's certificates chain.</span></span> <span data-ttu-id="d932f-108">Se qualquer certificado na cadeia for revogado, esse certificado e todos os certificados abaixo dele na cadeia também serão revogados.</span><span class="sxs-lookup"><span data-stu-id="d932f-108">If any certificate in the chain is revoked, then that certificate and all of the certificates below it in the chain are also revoked.</span></span>

<span data-ttu-id="d932f-109">Para obter a CRL, o aplicativo deve usar o Windows Media Format SDK, versão 9 ou posterior e executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d932f-109">To get the CRL, the application must use the Windows Media Format SDK, version 9 or later, and perform the following steps:</span></span>

1.  <span data-ttu-id="d932f-110">Chame **WMCreateReader** para criar o objeto leitor do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="d932f-110">Call **WMCreateReader** to create the Windows Media Format SDK reader object.</span></span>
2.  <span data-ttu-id="d932f-111">Consulte o objeto de leitor para a interface **IWMDRMReader** .</span><span class="sxs-lookup"><span data-stu-id="d932f-111">Query the reader object for the **IWMDRMReader** interface.</span></span>
3.  <span data-ttu-id="d932f-112">Chame **IWMDRMReader:: GetDRMProperty** com um valor de g \_ wszWMDRMNet \_ revogação para obter a CRL.</span><span class="sxs-lookup"><span data-stu-id="d932f-112">Call **IWMDRMReader::GetDRMProperty** with a value of g\_wszWMDRMNet\_Revocation to get the CRL.</span></span> <span data-ttu-id="d932f-113">Você deve chamar esse método duas vezes: uma vez para obter o tamanho do buffer a ser alocado e uma vez para preencher o buffer.</span><span class="sxs-lookup"><span data-stu-id="d932f-113">You must call this method twice: Once to get the size of the buffer to allocate, and once to fill the buffer.</span></span> <span data-ttu-id="d932f-114">A segunda chamada retorna uma cadeia de caracteres que contém a CRL.</span><span class="sxs-lookup"><span data-stu-id="d932f-114">The second call returns a string that contains the CRL.</span></span> <span data-ttu-id="d932f-115">A cadeia de caracteres inteira é codificada em base 64.</span><span class="sxs-lookup"><span data-stu-id="d932f-115">The entire string is base-64 encoded.</span></span>
4.  <span data-ttu-id="d932f-116">Decodifique a cadeia de caracteres codificada em base 64.</span><span class="sxs-lookup"><span data-stu-id="d932f-116">Decode the base-64 encoded string.</span></span> <span data-ttu-id="d932f-117">Você pode usar a função **CryptStringToBinary** para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="d932f-117">You can use the **CryptStringToBinary** function to do this.</span></span> <span data-ttu-id="d932f-118">Essa função faz parte do CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="d932f-118">This function is part of CryptoAPI.</span></span>

> [!Note]  
> <span data-ttu-id="d932f-119">Para usar a interface **IWMDRMReader** , você deve obter uma biblioteca de DRM estática da Microsoft e vincular seu aplicativo a esse arquivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d932f-119">To use the **IWMDRMReader** interface, you must obtain a static DRM library from Microsoft and link your application to this library file.</span></span> <span data-ttu-id="d932f-120">Para obter mais informações, consulte o tópico "obtendo a biblioteca de DRM necessária" na documentação do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d932f-120">For more information, see the topic "Obtaining the Required DRM Library" in the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="d932f-121">Se a CRL não estiver presente no computador do usuário, o método **GetDRMProperty** retornará a \_ \_ \_ Propriedade sem suporte do NS E DRM \_ .</span><span class="sxs-lookup"><span data-stu-id="d932f-121">If the CRL is not present on the user's computer, the **GetDRMProperty** method returns NS\_E\_DRM\_UNSUPPORTED\_PROPERTY.</span></span> <span data-ttu-id="d932f-122">Atualmente, a única maneira de obter a CRL é adquirir uma licença DRM.</span><span class="sxs-lookup"><span data-stu-id="d932f-122">Currently, the only way to obtain the CRL is to acquire a DRM license.</span></span>

<span data-ttu-id="d932f-123">O código a seguir mostra uma função que retorna a CRL:</span><span class="sxs-lookup"><span data-stu-id="d932f-123">The following code shows a function that returns the CRL:</span></span>


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



<span data-ttu-id="d932f-124">Em seguida, o aplicativo deve verificar se a CRL é válida.</span><span class="sxs-lookup"><span data-stu-id="d932f-124">Next, the application must verify that the CRL is valid.</span></span> <span data-ttu-id="d932f-125">Para fazer isso, verifique se o certificado de CRL, que faz parte da CRL, está assinado diretamente pelo certificado raiz da Microsoft e tem o valor do elemento SignCRL definido como 1.</span><span class="sxs-lookup"><span data-stu-id="d932f-125">To do so, verify that the CRL certificate, which is part of the CRL, is directly signed by the Microsoft Root Certificate and has the SignCRL element value set to 1.</span></span> <span data-ttu-id="d932f-126">Além disso, verifique a assinatura da CRL.</span><span class="sxs-lookup"><span data-stu-id="d932f-126">Also, verify the signature of the CRL.</span></span>

<span data-ttu-id="d932f-127">Depois que a CRL é verificada, o aplicativo pode armazená-la.</span><span class="sxs-lookup"><span data-stu-id="d932f-127">After the CRL is verified, the application can store it.</span></span> <span data-ttu-id="d932f-128">O número de versão da CRL também deve ser verificado antes do armazenamento para que o aplicativo sempre armazene a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="d932f-128">The CRL version number should also be checked before storing so that the application always stores the newest version.</span></span>

<span data-ttu-id="d932f-129">A CRL tem o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="d932f-129">The CRL has the following format.</span></span>



| <span data-ttu-id="d932f-130">Seção</span><span class="sxs-lookup"><span data-stu-id="d932f-130">Section</span></span>            | <span data-ttu-id="d932f-131">Sumário</span><span class="sxs-lookup"><span data-stu-id="d932f-131">Contents</span></span>                                                             |
|--------------------|----------------------------------------------------------------------|
| <span data-ttu-id="d932f-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d932f-132">Header</span></span>             | <span data-ttu-id="d932f-133">version32-bit CRL de 32 bits-número de entradas</span><span class="sxs-lookup"><span data-stu-id="d932f-133">32-bit CRL version32-bit number of entries</span></span>                           |
| <span data-ttu-id="d932f-134">Entradas de revogação</span><span class="sxs-lookup"><span data-stu-id="d932f-134">Revocation Entries</span></span> | <span data-ttu-id="d932f-135">Várias entradas de revogação de 160 bits</span><span class="sxs-lookup"><span data-stu-id="d932f-135">Multiple 160-bit revocation entries</span></span>                                  |
| <span data-ttu-id="d932f-136">Certificado</span><span class="sxs-lookup"><span data-stu-id="d932f-136">Certificate</span></span>        | <span data-ttu-id="d932f-137">certificado de comprimento lengthVariable do certificado de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d932f-137">32-bit certificate lengthVariable-length certificate</span></span>                 |
| <span data-ttu-id="d932f-138">Assinatura</span><span class="sxs-lookup"><span data-stu-id="d932f-138">Signature</span></span>          | <span data-ttu-id="d932f-139">assinatura de 8 bits type16-bit assinatura lengthVariable-assinatura de comprimento</span><span class="sxs-lookup"><span data-stu-id="d932f-139">8-bit signature type16-bit signature lengthVariable-length signature</span></span> |



 

> [!Note]  
> <span data-ttu-id="d932f-140">Todos os valores inteiros não são assinados e são representados na notação big endian (ordem de bytes de rede).</span><span class="sxs-lookup"><span data-stu-id="d932f-140">All integer values are unsigned and are represented in big-endian (network byte order) notation.</span></span>

 

<span data-ttu-id="d932f-141">Descrições da seção de CRL</span><span class="sxs-lookup"><span data-stu-id="d932f-141">CRL Section Descriptions</span></span>

<dl> <dt>

<span data-ttu-id="d932f-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Verga</span><span class="sxs-lookup"><span data-stu-id="d932f-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="d932f-143">O cabeçalho contém o número de versão da CRL e o número de entradas de revogação na CRL.</span><span class="sxs-lookup"><span data-stu-id="d932f-143">The header contains the version number of the CRL and the number of revocation entries in the CRL.</span></span> <span data-ttu-id="d932f-144">Uma CRL pode conter zero ou mais entradas.</span><span class="sxs-lookup"><span data-stu-id="d932f-144">A CRL can contain zero or more entries.</span></span>

</dd> <dt>

<span data-ttu-id="d932f-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Entradas de revogação</span><span class="sxs-lookup"><span data-stu-id="d932f-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Revocation entries</span></span>
</dt> <dd>

<span data-ttu-id="d932f-146">Cada entrada de revogação é o resumo de 160 bits de um certificado revogado.</span><span class="sxs-lookup"><span data-stu-id="d932f-146">Each revocation entry is the 160-bit digest of a revoked certificate.</span></span> <span data-ttu-id="d932f-147">Compare esse Resumo com o elemento DigestValue dentro do certificado.</span><span class="sxs-lookup"><span data-stu-id="d932f-147">Compare this digest with the DigestValue element within the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="d932f-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate</span><span class="sxs-lookup"><span data-stu-id="d932f-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate</span></span>
</dt> <dd>

<span data-ttu-id="d932f-149">A seção de certificado contém um valor de 32 bits que indica o comprimento (em bytes) do certificado XML e sua cadeia de certificados, juntamente com uma matriz de bytes que contém o certificado XML da autoridade de certificação (CA) e a cadeia de certificados que tem a Microsoft como raiz.</span><span class="sxs-lookup"><span data-stu-id="d932f-149">The certificate section contains a 32-bit value indicating the length (in bytes) of the XML certificate and its certificate chain, along with a byte array that contains both the XML certificate of the Certificate Authority (CA) and the certificate chain that has Microsoft as the Root.</span></span> <span data-ttu-id="d932f-150">O certificado deve ser assinado por uma autoridade de certificação que tenha autoridade para emitir CRLs.</span><span class="sxs-lookup"><span data-stu-id="d932f-150">The certificate must be signed by a CA that has the authority to issue CRLs.</span></span>

> [!Note]  
> <span data-ttu-id="d932f-151">O certificado não deve ser encerrado em nulo.</span><span class="sxs-lookup"><span data-stu-id="d932f-151">The certificate must not be null-terminated.</span></span>

 

</dd> <dt>

<span data-ttu-id="d932f-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span><span class="sxs-lookup"><span data-stu-id="d932f-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="d932f-153">A seção assinatura contém o tipo e o comprimento da assinatura e a própria assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="d932f-153">The signature section contains the signature type and length, and the digital signature itself.</span></span> <span data-ttu-id="d932f-154">O tipo de 8 bits é definido como 2 para indicar que ele usa SHA-1 com criptografia RSA de 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="d932f-154">The 8-bit type is set to 2 to indicate that it uses SHA-1 with 1024-bit RSA encryption.</span></span> <span data-ttu-id="d932f-155">O comprimento é um valor de 16 bits que contém o comprimento da assinatura digital em bytes.</span><span class="sxs-lookup"><span data-stu-id="d932f-155">The length is a 16-bit value containing the length of the digital signature in bytes.</span></span> <span data-ttu-id="d932f-156">A assinatura digital é calculada em todas as seções anteriores da CRL.</span><span class="sxs-lookup"><span data-stu-id="d932f-156">The digital signature is calculated over all prior sections of the CRL.</span></span>

<span data-ttu-id="d932f-157">A assinatura é calculada usando o esquema de assinatura digital RSASSA-PSS que é definido no PKCS \# 1 (versão 2,1).</span><span class="sxs-lookup"><span data-stu-id="d932f-157">The signature is calculated using the RSASSA-PSS digital signature scheme that is defined in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="d932f-158">A função de hash é SHA-1, que é definida em padrão FIPS (FIPS) 180-2, e a função de geração de máscara é MGF1, que é definida na seção B. 2.1 no PKCS \# 1 (versão 2,1).</span><span class="sxs-lookup"><span data-stu-id="d932f-158">The hash function is SHA-1, which is defined in Federal Information Processing Standard (FIPS) 180-2, and the mask generation function is MGF1, which is defined in section B.2.1 in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="d932f-159">As operações RSASP1 e RSAVP1 usam RSA com um módulo de 1024 bits com um expoente de verificação de 65537.</span><span class="sxs-lookup"><span data-stu-id="d932f-159">The RSASP1 and RSAVP1 operations use RSA with a 1024-bit modulus with a verification exponent of 65537.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d932f-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d932f-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d932f-161">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="d932f-161">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



