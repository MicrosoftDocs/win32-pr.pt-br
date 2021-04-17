---
description: A CNG permite criptografar dados usando um número mínimo de chamadas de função e permite que você execute todo o gerenciamento de memória.
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: Criptografando dados com CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f161cd23ec6863bee7f5ffd5b696fa99880e3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811810"
---
# <a name="encrypting-data-with-cng"></a><span data-ttu-id="ca888-103">Criptografando dados com CNG</span><span class="sxs-lookup"><span data-stu-id="ca888-103">Encrypting Data with CNG</span></span>

<span data-ttu-id="ca888-104">O uso principal de qualquer API de criptografia é criptografar e descriptografar dados.</span><span class="sxs-lookup"><span data-stu-id="ca888-104">The primary use of any cryptography API is to encrypt and decrypt data.</span></span> <span data-ttu-id="ca888-105">A CNG permite criptografar dados usando um número mínimo de chamadas de função e permite que você execute todo o gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="ca888-105">CNG allows you to encrypt data by using a minimum number of function calls and allows you to perform all of the memory management.</span></span> <span data-ttu-id="ca888-106">Embora muitos dos detalhes de implementação de protocolo tenham sido deixados para o usuário, a CNG fornece os primitivos que executam as tarefas reais de criptografia de dados e descriptografia.</span><span class="sxs-lookup"><span data-stu-id="ca888-106">While many of the protocol implementation details are left up to the user, CNG provides the primitives that perform the actual data encryption and decryption tasks.</span></span>

-   [<span data-ttu-id="ca888-107">Criptografando dados</span><span class="sxs-lookup"><span data-stu-id="ca888-107">Encrypting Data</span></span>](#encrypting-data-with-cng)
-   [<span data-ttu-id="ca888-108">Exemplo de criptografia de dados</span><span class="sxs-lookup"><span data-stu-id="ca888-108">Encrypting Data Example</span></span>](#encrypting-data-example)
-   [<span data-ttu-id="ca888-109">Descriptografando dados</span><span class="sxs-lookup"><span data-stu-id="ca888-109">Decrypting Data</span></span>](#decrypting-data)

## <a name="encrypting-data"></a><span data-ttu-id="ca888-110">Criptografando dados</span><span class="sxs-lookup"><span data-stu-id="ca888-110">Encrypting Data</span></span>

<span data-ttu-id="ca888-111">Para criptografar dados, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="ca888-111">To encrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="ca888-112">Abra um provedor de algoritmo que dê suporte à criptografia, como o **\_ \_ algoritmo BCRYPT des**.</span><span class="sxs-lookup"><span data-stu-id="ca888-112">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="ca888-113">Crie uma chave para criptografar os dados com.</span><span class="sxs-lookup"><span data-stu-id="ca888-113">Create a key to encrypt the data with.</span></span> <span data-ttu-id="ca888-114">Uma chave pode ser criada usando qualquer uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="ca888-114">A key can be created by using any of the following functions:</span></span>
    -   <span data-ttu-id="ca888-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) ou [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) para provedores assimétricos.</span><span class="sxs-lookup"><span data-stu-id="ca888-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) or [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) for asymmetric providers.</span></span>
    -   <span data-ttu-id="ca888-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) ou [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) para provedores simétricos.</span><span class="sxs-lookup"><span data-stu-id="ca888-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) or [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) for symmetric providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="ca888-117">A criptografia e descriptografia de dados com uma chave assimétrica é computacionalmente intensiva em comparação com a criptografia de chave simétrica.</span><span class="sxs-lookup"><span data-stu-id="ca888-117">Data encryption and decryption with an asymmetric key is computationally intensive compared to symmetric key encryption.</span></span> <span data-ttu-id="ca888-118">Se você precisar criptografar dados com uma chave assimétrica, deverá criptografar os dados com uma chave simétrica, criptografar a chave simétrica com uma chave assimétrica e incluir a chave simétrica criptografada com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca888-118">If you need to encrypt data with an asymmetric key, you should encrypt the data with a symmetric key, encrypt the symmetric key with an asymmetric key, and include the encrypted symmetric key with the message.</span></span> <span data-ttu-id="ca888-119">O destinatário pode então descriptografar a chave simétrica e usar a chave simétrica para descriptografar os dados.</span><span class="sxs-lookup"><span data-stu-id="ca888-119">The recipient can then decrypt the symmetric key and use the symmetric key to decrypt the data.</span></span>

     

3.  <span data-ttu-id="ca888-120">Obtenha o tamanho dos dados criptografados.</span><span class="sxs-lookup"><span data-stu-id="ca888-120">Obtain the size of the encrypted data.</span></span> <span data-ttu-id="ca888-121">Isso se baseia no algoritmo de criptografia, no esquema de preenchimento (se houver) e no tamanho dos dados a serem criptografados.</span><span class="sxs-lookup"><span data-stu-id="ca888-121">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be encrypted.</span></span> <span data-ttu-id="ca888-122">Você pode obter o tamanho dos dados criptografados usando a função [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) , passando **NULL** para o parâmetro *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="ca888-122">You can obtain the encrypted data size by using the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="ca888-123">Todos os outros parâmetros devem ser iguais a quando os dados são realmente criptografados, exceto pelo parâmetro *pbInput* , que não é usado nesse caso.</span><span class="sxs-lookup"><span data-stu-id="ca888-123">All other parameters must be the same as when the data is actually encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="ca888-124">Você pode criptografar os dados no local com o mesmo buffer ou criptografar os dados em um buffer separado.</span><span class="sxs-lookup"><span data-stu-id="ca888-124">You can either encrypt the data in place with the same buffer or encrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="ca888-125">Se você quiser criptografar os dados no local, passe o ponteiro do buffer de texto não criptografado para os parâmetros *pbInput* e *PbOutput* na função [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="ca888-125">If you want to encrypt the data in place, pass the plaintext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function.</span></span> <span data-ttu-id="ca888-126">É possível que o tamanho dos dados criptografados seja maior do que o tamanho dos dados não criptografados, portanto, o buffer de texto sem formatação deve ser grande o suficiente para manter os dados criptografados, não apenas o texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="ca888-126">It is possible that the encrypted data size will be larger than the unencrypted data size, so the plaintext buffer must be large enough to hold the encrypted data, not just the plaintext.</span></span> <span data-ttu-id="ca888-127">Você pode usar o tamanho obtido na etapa 3 para alocar o buffer de texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="ca888-127">You can use the size obtained in step 3 to allocate the plaintext buffer.</span></span>

    <span data-ttu-id="ca888-128">Se você quiser criptografar os dados em um buffer separado, aloque um buffer de memória para os dados criptografados usando o tamanho obtido na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="ca888-128">If you want to encrypt the data into a separate buffer, allocate a memory buffer for the encrypted data by using the size obtained in step 3.</span></span>

5.  <span data-ttu-id="ca888-129">Chame a função [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) para criptografar os dados.</span><span class="sxs-lookup"><span data-stu-id="ca888-129">Call the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function to encrypt the data.</span></span> <span data-ttu-id="ca888-130">Essa função gravará os dados criptografados no local fornecido no parâmetro *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="ca888-130">This function will write the encrypted data to the location provided in the *pbOutput* parameter.</span></span>
6.  <span data-ttu-id="ca888-131">Mantenha os dados criptografados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="ca888-131">Persist the encrypted data as needed.</span></span>
7.  <span data-ttu-id="ca888-132">Repita as etapas 5 e 6 até que todos os dados tenham sido criptografados.</span><span class="sxs-lookup"><span data-stu-id="ca888-132">Repeat steps 5 and 6 until all of the data has been encrypted.</span></span>

## <a name="encrypting-data-example"></a><span data-ttu-id="ca888-133">Exemplo de criptografia de dados</span><span class="sxs-lookup"><span data-stu-id="ca888-133">Encrypting Data Example</span></span>

<span data-ttu-id="ca888-134">O exemplo a seguir mostra como criptografar dados com a CNG usando o algoritmo de criptografia simétrica padrão de criptografia avançada.</span><span class="sxs-lookup"><span data-stu-id="ca888-134">The following example shows how to encrypt data with CNG by using the advanced encryption standard symmetric encryption algorithm.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:
    Sample program for AES-CBC encryption using CNG

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>

#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


#define DATA_TO_ENCRYPT  "Test Data"


const BYTE rgbPlaintext[] = 
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbIV[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07,
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbAES128Key[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

void PrintBytes(
                IN BYTE     *pbPrintData,
                IN DWORD    cbDataLen)
{
    DWORD dwCount = 0;

    for(dwCount=0; dwCount < cbDataLen;dwCount++)
    {
        printf("0x%02x, ",pbPrintData[dwCount]);

        if(0 == (dwCount + 1 )%10) putchar('\n');
    }

}

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAesAlg                     = NULL;
    BCRYPT_KEY_HANDLE       hKey                        = NULL;
    NTSTATUS                status                      = STATUS_UNSUCCESSFUL;
    DWORD                   cbCipherText                = 0, 
                            cbPlainText                 = 0,
                            cbData                      = 0, 
                            cbKeyObject                 = 0,
                            cbBlockLen                  = 0,
                            cbBlob                      = 0;
    PBYTE                   pbCipherText                = NULL,
                            pbPlainText                 = NULL,
                            pbKeyObject                 = NULL,
                            pbIV                        = NULL,
                            pbBlob                      = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);


    // Open an algorithm handle.
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAesAlg,
                                                BCRYPT_AES_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    // Calculate the size of the buffer to hold the KeyObject.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbKeyObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Allocate the key object on the heap.
    pbKeyObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbKeyObject);
    if(NULL == pbKeyObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   // Calculate the block length for the IV.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_BLOCK_LENGTH, 
                                        (PBYTE)&cbBlockLen, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Determine whether the cbBlockLen is not longer than the IV length.
    if (cbBlockLen > sizeof (rgbIV))
    {
        wprintf (L"**** block length is longer than the provided IV length\n");
        goto Cleanup;
    }

    // Allocate a buffer for the IV. The buffer is consumed during the 
    // encrypt/decrypt process.
    pbIV= (PBYTE) HeapAlloc (GetProcessHeap (), 0, cbBlockLen);
    if(NULL == pbIV)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbIV, rgbIV, cbBlockLen);

    if(!NT_SUCCESS(status = BCryptSetProperty(
                                hAesAlg, 
                                BCRYPT_CHAINING_MODE, 
                                (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
                                sizeof(BCRYPT_CHAIN_MODE_CBC), 
                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptSetProperty\n", status);
        goto Cleanup;
    }

                

     // Generate the key from supplied input key bytes.
    if(!NT_SUCCESS(status = BCryptGenerateSymmetricKey(
                                        hAesAlg, 
                                        &hKey, 
                                        pbKeyObject, 
                                        cbKeyObject, 
                                        (PBYTE)rgbAES128Key, 
                                        sizeof(rgbAES128Key), 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }

  
    // Save another copy of the key for later.
    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }


    // Allocate the buffer to hold the BLOB.
    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey, 
                                        NULL, 
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        pbBlob, 
                                        cbBlob, 
                                        &cbBlob, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }
 
    cbPlainText = sizeof(rgbPlaintext);
    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbPlainText, rgbPlaintext, sizeof(rgbPlaintext));
    
    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen,
                                        NULL, 
                                        0, 
                                        &cbCipherText, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    pbCipherText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbCipherText);
    if(NULL == pbCipherText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    // Use the key to encrypt the plaintext buffer.
    // For block sized messages, block padding will add an extra block.
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen, 
                                        pbCipherText, 
                                        cbCipherText, 
                                        &cbData, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    // Destroy the key and reimport from saved BLOB.
    if(!NT_SUCCESS(status = BCryptDestroyKey(hKey)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDestroyKey\n", status);
        goto Cleanup;
    }    
    hKey = 0;

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    pbPlainText = NULL;

    // We can reuse the key object.
    memset(pbKeyObject, 0 , cbKeyObject);

    
    // Reinitialize the IV because encryption would have modified it.
    memcpy(pbIV, rgbIV, cbBlockLen);


    if(!NT_SUCCESS(status = BCryptImportKey(
                                        hAesAlg,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        &hKey,
                                        pbKeyObject,
                                        cbKeyObject,
                                        pbBlob,
                                        cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }
       

    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV,
                                    cbBlockLen,
                                    NULL, 
                                    0, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }

    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV, 
                                    cbBlockLen,
                                    pbPlainText, 
                                    cbPlainText, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }


    if (0 != memcmp(pbPlainText, (PBYTE)rgbPlaintext, sizeof(rgbPlaintext))) 
    {
        wprintf(L"Expected decrypted text comparison failed.\n");
        goto Cleanup;
    } 

    wprintf(L"Success!\n");


Cleanup:

    if(hAesAlg)
    {
        BCryptCloseAlgorithmProvider(hAesAlg,0);
    }

    if (hKey)    
    {
        BCryptDestroyKey(hKey);
    }

    if(pbCipherText)
    {
        HeapFree(GetProcessHeap(), 0, pbCipherText);
    }

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    if(pbKeyObject)
    {
        HeapFree(GetProcessHeap(), 0, pbKeyObject);
    }

    if(pbIV)
    {
        HeapFree(GetProcessHeap(), 0, pbIV);
    }

}
```



## <a name="decrypting-data"></a><span data-ttu-id="ca888-135">Descriptografando dados</span><span class="sxs-lookup"><span data-stu-id="ca888-135">Decrypting Data</span></span>

<span data-ttu-id="ca888-136">Para descriptografar dados, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="ca888-136">To decrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="ca888-137">Abra um provedor de algoritmo que dê suporte à criptografia, como o **\_ \_ algoritmo BCRYPT des**.</span><span class="sxs-lookup"><span data-stu-id="ca888-137">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="ca888-138">Obtenha a chave com a qual os dados foram criptografados e use essa chave para obter um identificador para a chave.</span><span class="sxs-lookup"><span data-stu-id="ca888-138">Obtain the key that the data was encrypted with, and use that key to obtain a handle for the key.</span></span>
3.  <span data-ttu-id="ca888-139">Obter o tamanho dos dados descriptografados.</span><span class="sxs-lookup"><span data-stu-id="ca888-139">Obtain the size of the decrypted data.</span></span> <span data-ttu-id="ca888-140">Isso se baseia no algoritmo de criptografia, no esquema de preenchimento (se houver) e no tamanho dos dados a serem descriptografados.</span><span class="sxs-lookup"><span data-stu-id="ca888-140">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be decrypted.</span></span> <span data-ttu-id="ca888-141">Você pode obter o tamanho dos dados criptografados usando a função [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) , passando **NULL** para o parâmetro *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="ca888-141">You can obtain the encrypted data size by using the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="ca888-142">Os parâmetros que especificam o esquema de preenchimento e o [*vetor de inicialização*](/windows/desktop/SecGloss/i-gly) (IV) devem ser os mesmos que os dados foram criptografados, exceto o parâmetro *pbInput* , que não é usado nesse caso.</span><span class="sxs-lookup"><span data-stu-id="ca888-142">The parameters that specify the padding scheme and [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) must be the same as when the data was encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="ca888-143">Aloque um buffer de memória para os dados descriptografados.</span><span class="sxs-lookup"><span data-stu-id="ca888-143">Allocate a memory buffer for the decrypted data.</span></span>
5.  <span data-ttu-id="ca888-144">Você pode descriptografar os dados no local usando o mesmo buffer ou descriptografá-los em um buffer separado.</span><span class="sxs-lookup"><span data-stu-id="ca888-144">You can either decrypt the data in place by using the same buffer, or decrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="ca888-145">Se você quiser descriptografar os dados no local, passe o ponteiro do buffer de texto cifrado para os parâmetros *pbInput* e *PbOutput* na função [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="ca888-145">If you want to decrypt the data in place, pass the ciphertext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function.</span></span>

    <span data-ttu-id="ca888-146">Se você quiser descriptografar os dados em um buffer separado, aloque um buffer de memória para os dados descriptografados usando o tamanho obtido na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="ca888-146">If you want to decrypt the data into a separate buffer, allocate a memory buffer for the decrypted data by using the size obtained in step 3.</span></span>

6.  <span data-ttu-id="ca888-147">Chame a função [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) para descriptografar os dados.</span><span class="sxs-lookup"><span data-stu-id="ca888-147">Call the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function to decrypt the data.</span></span> <span data-ttu-id="ca888-148">Os parâmetros que especificam o esquema de preenchimento e IV devem ser iguais aos quando os dados foram criptografados.</span><span class="sxs-lookup"><span data-stu-id="ca888-148">The parameters that specify the padding scheme and IV must be the same as when the data was encrypted.</span></span> <span data-ttu-id="ca888-149">Essa função gravará os dados descriptografados no local fornecido no parâmetro *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="ca888-149">This function will write the decrypted data to the location provided in the *pbOutput* parameter.</span></span>
7.  <span data-ttu-id="ca888-150">Mantenha os dados descriptografados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="ca888-150">Persist the decrypted data as needed.</span></span>
8.  <span data-ttu-id="ca888-151">Repita as etapas 5 e 6 até que todos os dados tenham sido descriptografados.</span><span class="sxs-lookup"><span data-stu-id="ca888-151">Repeat steps 5 and 6 until all of the data has been decrypted.</span></span>

 

 
