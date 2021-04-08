---
description: O exemplo a seguir cria uma chave de sessão aleatória, duplica a chave, define alguns parâmetros adicionais na chave original e destrói as chaves original e duplicada.
ms.assetid: e57274cf-42d3-445b-97f1-dd574010290f
title: 'Programa de exemplo C: duplicando uma chave de sessão'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b38934d399a6a38f14e551e79d4e1f877dbadf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921611"
---
# <a name="example-c-program-duplicating-a-session-key"></a><span data-ttu-id="66b78-103">Programa de exemplo C: duplicando uma chave de sessão</span><span class="sxs-lookup"><span data-stu-id="66b78-103">Example C Program: Duplicating a Session Key</span></span>

<span data-ttu-id="66b78-104">O exemplo a seguir cria uma [*chave de sessão*](../secgloss/s-gly.md)aleatória, duplica a chave, define alguns parâmetros adicionais na chave original e destrói as chaves original e duplicada.</span><span class="sxs-lookup"><span data-stu-id="66b78-104">The following example creates a random [*session key*](../secgloss/s-gly.md), duplicates the key, sets some additional parameters on the original key, and destroys both the original and the duplicate keys.</span></span> <span data-ttu-id="66b78-105">Este exemplo ilustra o uso de [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey) e funções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="66b78-105">This example illustrates the use of [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey) and related functions.</span></span>

<span data-ttu-id="66b78-106">Este exemplo ilustra as seguintes tarefas e funções de CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="66b78-106">This example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="66b78-107">Acessando um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) usando [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span><span class="sxs-lookup"><span data-stu-id="66b78-107">Accessing a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="66b78-108">Criando uma chave de sessão usando [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span><span class="sxs-lookup"><span data-stu-id="66b78-108">Creating a session key using [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span></span>
-   <span data-ttu-id="66b78-109">Duplicando a chave criada usando [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey).</span><span class="sxs-lookup"><span data-stu-id="66b78-109">Duplicating the key created using [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey).</span></span>
-   <span data-ttu-id="66b78-110">Usando [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) para alterar o processo de geração de chave de duas maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="66b78-110">Using [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) to alter the key generation process in two different ways.</span></span>
-   <span data-ttu-id="66b78-111">Preenchendo um buffer com bytes aleatórios usando [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).</span><span class="sxs-lookup"><span data-stu-id="66b78-111">Filling a buffer with random bytes using [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).</span></span>
-   <span data-ttu-id="66b78-112">Destruindo as chaves usando [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="66b78-112">Destroying the keys using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span>
-   <span data-ttu-id="66b78-113">Liberando o CSP com o [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span><span class="sxs-lookup"><span data-stu-id="66b78-113">Releasing the CSP with [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span></span>

<span data-ttu-id="66b78-114">Este exemplo usa a função [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="66b78-114">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="66b78-115">O código para essa função está incluído no exemplo.</span><span class="sxs-lookup"><span data-stu-id="66b78-115">The code for this function is included with the sample.</span></span> <span data-ttu-id="66b78-116">O código para essa e outras funções auxiliares também está listado em [funções uso geral](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="66b78-116">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Begin main.

void main()
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV   hCryptProv;
HCRYPTKEY    hOriginalKey;
HCRYPTKEY    hDuplicateKey;
DWORD        dwMode;
BYTE         pbData[16];

//-------------------------------------------------------------------
// Begin processing.

printf("This program creates a session key and duplicates \n");
printf("that key. Next, parameters are added to the original \n");
printf("key. Finally, both keys are destroyed. \n\n");

//-------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(    
   &hCryptProv,
   NULL,
   NULL,
   PROV_RSA_FULL,
   0)) 
{    
    printf("CryptAcquireContext succeeded. \n");
}
else
{
    MyHandleError("Error during CryptAcquireContext!\n");
}
//-------------------------------------------------------------------
// Generate a key.
if (CryptGenKey(
     hCryptProv, 
     CALG_RC4, 
     0, 
     &hOriginalKey))
{
   printf("Original session key is created. \n");
}
else
{
   MyHandleError("ERROR - CryptGenKey.");
}
//-------------------------------------------------------------------
// Duplicate the key.

if (CryptDuplicateKey(
     hOriginalKey, 
     NULL, 
     0, 
     &hDuplicateKey))
{
   printf("The session key has been duplicated. \n");
}
else
{
   MyHandleError("ERROR - CryptDuplicateKey");
}
//-------------------------------------------------------------------
// Set additional parameters on the original key.
// First, set the cipher mode.

dwMode = CRYPT_MODE_ECB;
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_MODE, 
   (BYTE*)&dwMode, 
   0)) 
{
     printf("Key Parameters set. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
// Generate a random initialization vector.
if(CryptGenRandom(
   hCryptProv, 
   8, 
   pbData)) 
{
     printf("Random sequence generated. \n");
}
else
{
     MyHandleError("Error during CryptGenRandom.");
}
//-------------------------------------------------------------------
// Set the initialization vector.
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_IV, 
   pbData, 
   0)) 
{
     printf("Parameter set with random sequence as "
         "initialization vector. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
//-------------------------------------------------------------------
// Clean up.

if (hOriginalKey)
    if (!CryptDestroyKey(hOriginalKey))
        MyHandleError("Failed CryptDestroyKey\n");

if (hDuplicateKey)
    if (!CryptDestroyKey(hDuplicateKey))
            MyHandleError("Failed CryptDestroyKey\n");

if(hCryptProv)
    if (!CryptReleaseContext(hCryptProv, 0))
        MyHandleError("Failed CryptReleaseContext\n");

printf("\nThe program ran to completion without error. \n");

} // End of main.

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message and exit 
//  the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 
