---
description: A assinatura de dados não protege os dados. Apenas para verificar a integridade dos dados.
ms.assetid: 8f0ace5a-c8f9-4a45-8500-041a9f22637d
title: Assinando dados com CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658dd1c9a833cfb15b708a7f85013e3d9cacac9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091442"
---
# <a name="signing-data-with-cng"></a>Assinando dados com CNG

A assinatura de dados não protege os dados. Apenas para verificar a integridade dos dados. O remetente armazena em hash que os dados e sinais (criptografa) o hash usando uma chave privada. O destinatário pretendido executa a verificação criando um hash dos dados recebidos, descriptografando a assinatura para obter o hash original e comparando os dois hashes.

Quando os dados são assinados, o remetente cria um valor de [*hash*](/windows/desktop/SecGloss/h-gly) e assina (criptografa) o hash usando uma chave privada. Essa assinatura é então anexada aos dados e enviada em uma mensagem para um destinatário. O algoritmo de hash que foi usado para criar a assinatura deve ser conhecido com antecedência pelo destinatário ou identificado na mensagem. A forma como isso é feito é o protocolo de mensagem.

Para verificar a assinatura, o destinatário extrai os dados e a assinatura da mensagem. Em seguida, o destinatário cria outro valor de hash a partir dos dados, descriptografa o hash assinado usando a chave pública do remetente e compara os dois valores de hash. Se os valores forem idênticos, a assinatura foi verificada e os dados serão considerados inalterados.

**Para criar uma assinatura usando CNG**

1.  Crie um valor de hash para os dados usando as funções de hash CNG. Para obter mais informações sobre como criar um hash, consulte [criando um hash com a CNG](creating-a-hash-with-cng.md).
2.  Crie uma chave assimétrica para assinar o hash. Você pode criar uma chave persistente com as [funções de armazenamento de chave CNG](cng-key-storage-functions.md) ou uma chave efêmera com as [funções primitivas de criptografia CNG](cng-cryptographic-primitive-functions.md).
3.  Use a função [**NCryptSignHash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) ou [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) para assinar (criptografar) o valor de hash. Essa função assina o valor de hash usando a chave assimétrica.
4.  Combine os dados e a assinatura em uma mensagem que pode ser enviada para o destinatário pretendido.

**Para verificar uma assinatura usando CNG**

1.  Extraia os dados e a assinatura da mensagem.
2.  Crie um valor de hash para os dados usando as funções de hash CNG. O algoritmo de hash usado deve ser o mesmo algoritmo usado para assinar o hash.
3.  Obtenha a parte pública do par de chaves assimétricas que foi usada para assinar o hash. A forma como você obtém essa chave depende de como a chave foi criada e persistida. Se a chave tiver sido criada ou carregada com as [funções de armazenamento de chaves CNG](cng-key-storage-functions.md), você usará a função [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) para carregar a chave persistente. Se a chave for uma chave efêmera, ela precisará ter sido salva em um BLOB de chave. Você precisa passar esse BLOB de chave para a função [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) ou [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) .
4.  Passe o novo valor de hash, a assinatura e o identificador de chave para a função [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) ou [**BCryptVerifySignature**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) . Essas funções executam a verificação usando a chave pública para descriptografar a assinatura e comparar o hash descriptografado com o hash calculado na etapa 2. A função **BCryptVerifySignature** retornará o **status \_ Success** se a assinatura corresponder à assinatura de hash ou de **status \_ \_ inválida** se a assinatura não corresponder ao hash. A função **NCryptVerifySignature** retornará o **status \_ Success** se a assinatura corresponder ao hash ou **à \_ \_ assinatura incorreta do nte** se a assinatura não corresponder ao hash.

## <a name="signing-and-verifying-data-example"></a>Exemplo de assinatura e verificação de dados

O exemplo a seguir mostra como usar as APIs primitivas de criptografia para assinar dados com uma chave persistente e verificar a assinatura com uma chave efêmera.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for ECDSA 256 signing using CNG
    
    Example for use of BCrypt/NCrypt API
    
    Persisted key for signing and ephemeral key for verification

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>
#include <ncrypt.h>


#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const  BYTE rgbMsg[] =
{
    0x04, 0x87, 0xec, 0x66, 0xa8, 0xbf, 0x17, 0xa6,
    0xe3, 0x62, 0x6f, 0x1a, 0x55, 0xe2, 0xaf, 0x5e,
    0xbc, 0x54, 0xa4, 0xdc, 0x68, 0x19, 0x3e, 0x94,
};

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{
    NCRYPT_PROV_HANDLE      hProv           = NULL;
    NCRYPT_KEY_HANDLE       hKey            = NULL;
    BCRYPT_KEY_HANDLE       hTmpKey         = NULL;
    SECURITY_STATUS         secStatus       = ERROR_SUCCESS;
    BCRYPT_ALG_HANDLE       hHashAlg        = NULL,
                            hSignAlg        = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbBlob          = 0,
                            cbSignature     = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL,
                            pbBlob          = NULL,
                            pbSignature     = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hHashAlg,
                                                BCRYPT_SHA1_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hSignAlg,
                                                BCRYPT_ECDSA_P256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hHashAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbHashObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash object on the heap
    pbHashObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHashObject);
    if(NULL == pbHashObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   //calculate the length of the hash
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hHashAlg, 
                                        BCRYPT_HASH_LENGTH, 
                                        (PBYTE)&cbHash, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash buffer on the heap
    pbHash = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHash);
    if(NULL == pbHash)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    //create a hash
    if(!NT_SUCCESS(status = BCryptCreateHash(
                                        hHashAlg, 
                                        &hHash, 
                                        pbHashObject, 
                                        cbHashObject, 
                                        NULL, 
                                        0, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptCreateHash\n", status);
        goto Cleanup;
    }
    

    //hash some data
    if(!NT_SUCCESS(status = BCryptHashData(
                                        hHash,
                                        (PBYTE)rgbMsg,
                                        sizeof(rgbMsg),
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptHashData\n", status);
        goto Cleanup;
    }
    
    //close the hash
    if(!NT_SUCCESS(status = BCryptFinishHash(
                                        hHash, 
                                        pbHash, 
                                        cbHash, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptFinishHash\n", status);
        goto Cleanup;
    }

    //open handle to KSP
    if(FAILED(secStatus = NCryptOpenStorageProvider(
                                                &hProv, 
                                                MS_KEY_STORAGE_PROVIDER, 
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptOpenStorageProvider\n", secStatus);
        goto Cleanup;
    }

    //create a persisted key
    if(FAILED(secStatus = NCryptCreatePersistedKey(
                                                hProv,
                                                &hKey,
                                                NCRYPT_ECDSA_P256_ALGORITHM,
                                                L"my ecc key",
                                                0,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptCreatePersistedKey\n", secStatus);
        goto Cleanup;
    }

    //create key on disk
    if(FAILED(secStatus = NCryptFinalizeKey(hKey, 0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptFinalizeKey\n", secStatus);
        goto Cleanup;
    }

    //sign the hash
    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    NULL,
                                    0,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }


    //allocate the signature buffer
    pbSignature = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbSignature);
    if(NULL == pbSignature)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    pbSignature,
                                    cbSignature,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        pbBlob,
                                        cbBlob,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptImportKeyPair(
                                            hSignAlg,
                                            NULL,
                                            BCRYPT_ECCPUBLIC_BLOB,
                                            &hTmpKey,
                                            pbBlob,
                                            cbBlob,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptImportKeyPair\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptVerifySignature(
                                            hTmpKey,
                                            NULL,
                                            pbHash,
                                            cbHash,
                                            pbSignature,
                                            cbSignature,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptVerifySignature\n", status);
        goto Cleanup;
    }

    wprintf(L"Success!\n");

Cleanup:

    if(hHashAlg)
    {
        BCryptCloseAlgorithmProvider(hHashAlg,0);
    }

    if(hSignAlg)
    {
        BCryptCloseAlgorithmProvider(hSignAlg,0);
    }

    if (hHash)    
    {
        BCryptDestroyHash(hHash);
    }

    if(pbHashObject)
    {
        HeapFree(GetProcessHeap(), 0, pbHashObject);
    }

    if(pbHash)
    {
        HeapFree(GetProcessHeap(), 0, pbHash);
    }

    if(pbSignature)
    {
        HeapFree(GetProcessHeap(), 0, pbSignature);
    }

    if(pbBlob)
    {
        HeapFree(GetProcessHeap(), 0, pbBlob);
    }

    if (hTmpKey)    
    {
        BCryptDestroyKey(hTmpKey);
    }

    if (hKey)    
    {
        NCryptDeleteKey(hKey, 0);
    }

    if (hProv)    
    {
        NCryptFreeObject(hProv);
    }    
}


```



 

 
