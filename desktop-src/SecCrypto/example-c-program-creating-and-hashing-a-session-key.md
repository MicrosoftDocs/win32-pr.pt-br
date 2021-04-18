---
description: Cria e aplica hash a uma chave de sessão que pode ser usada para criptografar uma mensagem, texto ou arquivo.
ms.assetid: 15d4a05d-5888-4532-91fd-6cd94afe0b99
title: 'Programa C de exemplo: Criando e aplicando hash a uma chave de sessão'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbfb1dae0f331a80a2b2c473f0446cf2a1623dda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760390"
---
# <a name="example-c-program-creating-and-hashing-a-session-key"></a><span data-ttu-id="cb118-103">Programa C de exemplo: Criando e aplicando hash a uma chave de sessão</span><span class="sxs-lookup"><span data-stu-id="cb118-103">Example C Program: Creating and Hashing a Session Key</span></span>

<span data-ttu-id="cb118-104">O exemplo a seguir cria e [*aplica hash*](../secgloss/h-gly.md) a uma [*chave de sessão*](../secgloss/s-gly.md) que pode ser usada para criptografar uma mensagem, texto ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="cb118-104">The following example creates and [*hashes*](../secgloss/h-gly.md) a [*session key*](../secgloss/s-gly.md) that can be used to encrypt a message, text, or file.</span></span>

<span data-ttu-id="cb118-105">Este exemplo também mostra como usar as seguintes funções de CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="cb118-105">This example also shows using the following CryptoAPI functions:</span></span>

-   <span data-ttu-id="cb118-106">[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para adquirir um [*provedor de serviços de criptografia*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cb118-106">[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) to acquire a [*cryptographic service provider*](../secgloss/c-gly.md).</span></span>
-   <span data-ttu-id="cb118-107">[**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) para criar um objeto hash vazio.</span><span class="sxs-lookup"><span data-stu-id="cb118-107">[**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) to create an empty hash object.</span></span>
-   <span data-ttu-id="cb118-108">[**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para criar uma [*chave de sessão*](../secgloss/s-gly.md)aleatória.</span><span class="sxs-lookup"><span data-stu-id="cb118-108">[**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) to create a random [*session key*](../secgloss/s-gly.md).</span></span>
-   <span data-ttu-id="cb118-109">[**CryptHashSessionKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) para o hash da chave de sessão criada.</span><span class="sxs-lookup"><span data-stu-id="cb118-109">[**CryptHashSessionKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) to hash the session key created.</span></span>
-   <span data-ttu-id="cb118-110">[**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) para destruir o hash.</span><span class="sxs-lookup"><span data-stu-id="cb118-110">[**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) to destroy the hash.</span></span>
-   <span data-ttu-id="cb118-111">[**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) para destruir a chave criada.</span><span class="sxs-lookup"><span data-stu-id="cb118-111">[**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) to destroy the key created.</span></span>
-   <span data-ttu-id="cb118-112">[**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) para liberar o CSP.</span><span class="sxs-lookup"><span data-stu-id="cb118-112">[**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) to release the CSP.</span></span>

<span data-ttu-id="cb118-113">Este exemplo usa a função [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="cb118-113">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="cb118-114">O código para essa função está incluído no exemplo.</span><span class="sxs-lookup"><span data-stu-id="cb118-114">The code for this function is included with the sample.</span></span> <span data-ttu-id="cb118-115">O código para essa e outras funções auxiliares também está listado em [funções uso geral](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cb118-115">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//  Copyright (C) Microsoft. All rights reserved.
//  
//  CreateAndHashSessionKey.cpp : Defines the entry point for the 
//  application.
//

#include <stdafx.h>

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(LPTSTR psz);

void main()
{
    HCRYPTPROV hCryptProv;
    HCRYPTHASH hHash;
    HCRYPTKEY hKey;

    //---------------------------------------------------------------
    // Acquire a cryptographic provider context handle.
    if(CryptAcquireContext(
        &hCryptProv, 
        NULL, 
        NULL, 
        PROV_RSA_FULL, 
        0)) 
    {
        printf("CryptAcquireContext complete. \n");
    }
    else
    {
        MyHandleError("Acquisition of context failed.");
    }

    //---------------------------------------------------------------
    // Create a hash object.
    if(CryptCreateHash(
        hCryptProv, 
        CALG_MD5, 
        0, 
        0, 
        &hHash)) 
    {
        printf("An empty hash object has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptBeginHash!\n");
    }

    //---------------------------------------------------------------
    // Create a random session key.
    if(CryptGenKey(
        hCryptProv, 
        CALG_RC2, 
        CRYPT_EXPORTABLE, 
        &hKey)) 
    {
        printf("A random session key has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptGenKey!\n");
    }

    //---------------------------------------------------------------
    // Compute the cryptographic hash on the key object.
    if(CryptHashSessionKey(
        hHash, 
        hKey, 
        0))
    {
        printf("The session key has been hashed. \n");
    }
    else
    {
        MyHandleError("Error during CryptHashSessionKey!\n");
    }

    /*
    Use the hash of the key object. For instance, additional data 
    could be hashed and sent in a message to several recipients. The 
    recipients will be able to verify who the message originator is 
    if the key used is also exported to them.
    */

    //---------------------------------------------------------------
    // Clean up.

    // Destroy the hash object.

    if(hHash)
    {
        if(!(CryptDestroyHash(hHash)))
        {
            MyHandleError("Error during CryptDestroyHash");
        }
    }

    // Destroy the session key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError("Error during CryptDestroyKey");
        }
    }

    // Release the provider.
    if(hCryptProv)
    {
        if(!(CryptReleaseContext(hCryptProv,0)))
        {
            MyHandleError("Error during CryptReleaseContext");
        }
    }
} // End main.

//  Define function MyHandleError.
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

```



 

 
