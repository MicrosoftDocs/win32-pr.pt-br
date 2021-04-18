---
description: Os hashes são mais úteis para verificar a integridade dos dados quando usados com um algoritmo de assinatura assimétrica.
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: Criando um hash com CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735f95182b63facee687f408ea4a07e09399e562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757080"
---
# <a name="creating-a-hash-with-cng"></a><span data-ttu-id="6a676-103">Criando um hash com CNG</span><span class="sxs-lookup"><span data-stu-id="6a676-103">Creating a Hash with CNG</span></span>

<span data-ttu-id="6a676-104">Um [*hash*](/windows/desktop/SecGloss/h-gly) é uma operação unidirecional que é executada em um bloco de dados para criar um valor de hash exclusivo que representa o conteúdo dos dados.</span><span class="sxs-lookup"><span data-stu-id="6a676-104">A [*hash*](/windows/desktop/SecGloss/h-gly) is a one way operation that is performed on a block of data to create a unique hash value that represents the contents of the data.</span></span> <span data-ttu-id="6a676-105">Não importa quando o hash é executado, o mesmo [*algoritmo de hash*](/windows/desktop/SecGloss/h-gly) executado nos mesmos dados sempre produzirá o mesmo valor de hash.</span><span class="sxs-lookup"><span data-stu-id="6a676-105">No matter when the hash is performed, the same [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) performed on the same data will always produce the same hash value.</span></span> <span data-ttu-id="6a676-106">Se qualquer um dos dados for alterado, o valor de hash será alterado adequadamente.</span><span class="sxs-lookup"><span data-stu-id="6a676-106">If any of the data changes, the hash value will change appropriately.</span></span>

<span data-ttu-id="6a676-107">Os hashes não são úteis para criptografar dados porque não se destinam a serem usados para reproduzir os dados originais do valor de hash.</span><span class="sxs-lookup"><span data-stu-id="6a676-107">Hashes are not useful for encrypting data because they are not intended to be used to reproduce the original data from the hash value.</span></span> <span data-ttu-id="6a676-108">Os hashes são mais úteis para verificar a integridade dos dados quando usados com um algoritmo de assinatura assimétrica.</span><span class="sxs-lookup"><span data-stu-id="6a676-108">Hashes are most useful to verify the integrity of the data when used with an asymmetric signing algorithm.</span></span> <span data-ttu-id="6a676-109">Por exemplo, se você tiver um hash de uma mensagem de texto, assinado o hash e incluído o valor de hash assinado com a mensagem original, o destinatário poderá verificar o hash assinado, criar o valor de hash da mensagem recebida e comparar esse valor de hash com o valor de hash assinado incluído com a mensagem original.</span><span class="sxs-lookup"><span data-stu-id="6a676-109">For example, if you hashed a text message, signed the hash, and included the signed hash value with the original message, the recipient could verify the signed hash, create the hash value for the received message, and then compare this hash value with the signed hash value included with the original message.</span></span> <span data-ttu-id="6a676-110">Se os dois valores de hash forem idênticos, o destinatário poderá ser razoavelmente certo de que a mensagem original não foi modificada.</span><span class="sxs-lookup"><span data-stu-id="6a676-110">If the two hash values are identical, the recipient can be reasonably sure that the original message has not been modified.</span></span>

<span data-ttu-id="6a676-111">O tamanho do valor de hash é fixo para um algoritmo de hash específico.</span><span class="sxs-lookup"><span data-stu-id="6a676-111">The size of the hash value is fixed for a particular hashing algorithm.</span></span> <span data-ttu-id="6a676-112">Isso significa que, independentemente do tamanho do bloco de dados grande ou pequeno, o valor de hash sempre será o mesmo.</span><span class="sxs-lookup"><span data-stu-id="6a676-112">What this means is that no matter how large or small the data block is, the hash value will always be the same size.</span></span> <span data-ttu-id="6a676-113">Por exemplo, o algoritmo de hash SHA256 tem um tamanho de valor de hash de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="6a676-113">As an example, the SHA256 hashing algorithm has a hash value size of 256 bits.</span></span>

-   [<span data-ttu-id="6a676-114">Criando um objeto de hash</span><span class="sxs-lookup"><span data-stu-id="6a676-114">Creating a Hashing Object</span></span>](#creating-a-hashing-object)
-   [<span data-ttu-id="6a676-115">Criando um objeto de hash reutilizável</span><span class="sxs-lookup"><span data-stu-id="6a676-115">Creating a Reusable Hashing Object</span></span>](#creating-a-reusable-hashing-object)
-   [<span data-ttu-id="6a676-116">Duplicando um objeto de hash</span><span class="sxs-lookup"><span data-stu-id="6a676-116">Duplicating a Hash Object</span></span>](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a><span data-ttu-id="6a676-117">Criando um objeto de hash</span><span class="sxs-lookup"><span data-stu-id="6a676-117">Creating a Hashing Object</span></span>

<span data-ttu-id="6a676-118">Para criar um hash usando a CNG, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="6a676-118">To create a hash using CNG, perform the following steps:</span></span>

1.  <span data-ttu-id="6a676-119">Abra um provedor de algoritmo que dê suporte ao algoritmo desejado.</span><span class="sxs-lookup"><span data-stu-id="6a676-119">Open an algorithm provider that supports the desired algorithm.</span></span> <span data-ttu-id="6a676-120">Os algoritmos de hash típicos incluem MD2, MD4, MD5, SHA-1 e SHA256.</span><span class="sxs-lookup"><span data-stu-id="6a676-120">Typical hashing algorithms include MD2, MD4, MD5, SHA-1, and SHA256.</span></span> <span data-ttu-id="6a676-121">Chame a função [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e especifique o identificador de algoritmo apropriado no parâmetro *pszAlgId* .</span><span class="sxs-lookup"><span data-stu-id="6a676-121">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter.</span></span> <span data-ttu-id="6a676-122">A função retorna um identificador para o provedor.</span><span class="sxs-lookup"><span data-stu-id="6a676-122">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="6a676-123">Execute as seguintes etapas para criar o objeto de hash:</span><span class="sxs-lookup"><span data-stu-id="6a676-123">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="6a676-124">Obtenha o tamanho do objeto chamando a função [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para recuperar a propriedade de **\_ \_ comprimento do objeto BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="6a676-124">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="6a676-125">Aloque memória para manter o objeto de hash.</span><span class="sxs-lookup"><span data-stu-id="6a676-125">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="6a676-126">Crie o objeto chamando a função [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="6a676-126">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span>

3.  <span data-ttu-id="6a676-127">Hash dos dados.</span><span class="sxs-lookup"><span data-stu-id="6a676-127">Hash the data.</span></span> <span data-ttu-id="6a676-128">Isso envolve chamar a função [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) uma ou mais vezes.</span><span class="sxs-lookup"><span data-stu-id="6a676-128">This involves calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function one or more times.</span></span> <span data-ttu-id="6a676-129">Cada chamada acrescenta os dados especificados ao hash.</span><span class="sxs-lookup"><span data-stu-id="6a676-129">Each call appends the specified data to the hash.</span></span>
4.  <span data-ttu-id="6a676-130">Execute as seguintes etapas para obter o valor de hash:</span><span class="sxs-lookup"><span data-stu-id="6a676-130">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="6a676-131">Recupere o tamanho do valor chamando a função [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para obter a propriedade de **\_ \_ comprimento de hash BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="6a676-131">Retrieve the size of the value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="6a676-132">Aloque memória para manter o valor.</span><span class="sxs-lookup"><span data-stu-id="6a676-132">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="6a676-133">Recupere o valor de hash chamando a função [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) .</span><span class="sxs-lookup"><span data-stu-id="6a676-133">Retrieve the hash value by calling the [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) function.</span></span> <span data-ttu-id="6a676-134">Depois que essa função for chamada, o objeto hash não será mais válido.</span><span class="sxs-lookup"><span data-stu-id="6a676-134">After this function has been called, the hash object is no longer valid.</span></span>

5.  <span data-ttu-id="6a676-135">Para concluir este procedimento, você deve executar as seguintes etapas de limpeza:</span><span class="sxs-lookup"><span data-stu-id="6a676-135">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="6a676-136">Feche o objeto de hash passando o identificador de hash para a função [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="6a676-136">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="6a676-137">Libere a memória alocada para o objeto de hash.</span><span class="sxs-lookup"><span data-stu-id="6a676-137">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="6a676-138">Se você não estiver criando mais objetos hash, feche o provedor de algoritmos passando o identificador do provedor para a função [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="6a676-138">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>

        <span data-ttu-id="6a676-139">Se você for criar mais objetos de hash, sugerimos que você reutilize o provedor de algoritmo em vez de criar e destruir o mesmo tipo de provedor de algoritmo muitas vezes.</span><span class="sxs-lookup"><span data-stu-id="6a676-139">If you will be creating more hash objects, we suggest you reuse the algorithm provider rather than creating and destroying the same type of algorithm provider many times.</span></span>

    4.  <span data-ttu-id="6a676-140">Quando você terminar de usar a memória de valor de hash, libere-a.</span><span class="sxs-lookup"><span data-stu-id="6a676-140">When you have finished using the hash value memory, free it.</span></span>

<span data-ttu-id="6a676-141">O exemplo a seguir mostra como criar um valor de hash usando a CNG.</span><span class="sxs-lookup"><span data-stu-id="6a676-141">The following example shows how to create a hash value by using CNG.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for SHA 256 hashing using CNG

--*/


#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>



#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const BYTE rgbMsg[] = 
{
    0x61, 0x62, 0x63
};


void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAlg            = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAlg,
                                                BCRYPT_SHA256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
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
                                        hAlg, 
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
                                        hAlg, 
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

    wprintf(L"Success!\n");

Cleanup:

    if(hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg,0);
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

}

```



## <a name="creating-a-reusable-hashing-object"></a><span data-ttu-id="6a676-142">Criando um objeto de hash reutilizável</span><span class="sxs-lookup"><span data-stu-id="6a676-142">Creating a Reusable Hashing Object</span></span>

<span data-ttu-id="6a676-143">A partir do Windows 8 e do Windows Server 2012, você pode criar um objeto de hash reutilizável para cenários que exigem a computação de vários hashes ou HMACs em uma rápida sucessão.</span><span class="sxs-lookup"><span data-stu-id="6a676-143">Beginning with Windows 8 and Windows Server 2012, you can create a reusable hashing object for scenarios that require you to compute multiple hashes or HMACs in rapid succession.</span></span> <span data-ttu-id="6a676-144">Faça isso especificando o **sinalizador BCRYPT \_ hash \_ reutilizável \_** ao chamar a função [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="6a676-144">Do this by specifying the **BCRYPT\_HASH\_REUSABLE\_FLAG** when calling the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function.</span></span> <span data-ttu-id="6a676-145">Todos os provedores de algoritmos de hash da Microsoft dão suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6a676-145">All Microsoft hash algorithm providers support this flag.</span></span> <span data-ttu-id="6a676-146">Um objeto de hash criado com esse sinalizador pode ser reutilizado imediatamente após chamar [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) , como se ele tivesse sido criado de forma nova, chamando [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="6a676-146">A hashing object created by using this flag can be reused immediately after calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) just as if it had been freshly created by calling [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span></span> <span data-ttu-id="6a676-147">Execute as seguintes etapas para criar um objeto de hash reutilizável:</span><span class="sxs-lookup"><span data-stu-id="6a676-147">Perform the following steps to create a reusable hashing object:</span></span>

1.  <span data-ttu-id="6a676-148">Abra um provedor de algoritmo que dê suporte ao algoritmo de hash desejado.</span><span class="sxs-lookup"><span data-stu-id="6a676-148">Open an algorithm provider that supports the desired hashing algorithm.</span></span> <span data-ttu-id="6a676-149">Chame a função [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e especifique o identificador de algoritmo apropriado no parâmetro *pszAlgId* e **no \_ \_ \_ sinalizador BCRYPT hash reutilizável** no parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6a676-149">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter and **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span> <span data-ttu-id="6a676-150">A função retorna um identificador para o provedor.</span><span class="sxs-lookup"><span data-stu-id="6a676-150">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="6a676-151">Execute as seguintes etapas para criar o objeto de hash:</span><span class="sxs-lookup"><span data-stu-id="6a676-151">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="6a676-152">Obtenha o tamanho do objeto chamando a função [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para recuperar a propriedade de **\_ \_ comprimento do objeto BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="6a676-152">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="6a676-153">Aloque memória para manter o objeto de hash.</span><span class="sxs-lookup"><span data-stu-id="6a676-153">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="6a676-154">Crie o objeto chamando a função [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="6a676-154">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="6a676-155">Especifique **o \_ \_ \_ sinalizador de hash reutilizável de BCRYPT** no parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6a676-155">Specify **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span>

3.  <span data-ttu-id="6a676-156">Hash dos dados chamando a função [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="6a676-156">Hash the data by calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function.</span></span>
4.  <span data-ttu-id="6a676-157">Execute as seguintes etapas para obter o valor de hash:</span><span class="sxs-lookup"><span data-stu-id="6a676-157">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="6a676-158">Obtenha o tamanho do valor de hash chamando a função [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para obter a propriedade **de \_ \_ comprimento de hash BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="6a676-158">Obtain the size of the hash value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="6a676-159">Aloque memória para manter o valor.</span><span class="sxs-lookup"><span data-stu-id="6a676-159">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="6a676-160">Obtenha o valor de hash chamando [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span><span class="sxs-lookup"><span data-stu-id="6a676-160">Get the hash value by calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span></span>

5.  <span data-ttu-id="6a676-161">Para reutilizar o objeto de hash com novos dados, vá para a etapa 3.</span><span class="sxs-lookup"><span data-stu-id="6a676-161">To reuse the hashing object with new data, go to step 3.</span></span>
6.  <span data-ttu-id="6a676-162">Para concluir este procedimento, você deve executar as seguintes etapas de limpeza:</span><span class="sxs-lookup"><span data-stu-id="6a676-162">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="6a676-163">Feche o objeto de hash passando o identificador de hash para a função [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="6a676-163">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="6a676-164">Libere a memória alocada para o objeto de hash.</span><span class="sxs-lookup"><span data-stu-id="6a676-164">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="6a676-165">Se você não estiver criando mais objetos hash, feche o provedor de algoritmos passando o identificador do provedor para a função [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="6a676-165">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>
    4.  <span data-ttu-id="6a676-166">Quando você terminar de usar a memória de valor de hash, libere-a.</span><span class="sxs-lookup"><span data-stu-id="6a676-166">When you have finished using the hash value memory, free it.</span></span>

## <a name="duplicating-a-hash-object"></a><span data-ttu-id="6a676-167">Duplicando um objeto de hash</span><span class="sxs-lookup"><span data-stu-id="6a676-167">Duplicating a Hash Object</span></span>

<span data-ttu-id="6a676-168">Em algumas circunstâncias, pode ser útil fazer hash de alguma quantidade de dados comuns e, em seguida, criar dois objetos de hash separados a partir dos dados comuns.</span><span class="sxs-lookup"><span data-stu-id="6a676-168">In some circumstances, it may be useful to hash some amount of common data and then create two separate hash objects from the common data.</span></span> <span data-ttu-id="6a676-169">Você não precisa criar dois objetos de hash separados e aplicar o hash aos dados comuns duas vezes para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="6a676-169">You do not have to create two separate hash objects and hash the common data twice to accomplish this.</span></span> <span data-ttu-id="6a676-170">Você pode criar um único objeto de hash e adicionar todos os dados comuns ao objeto de hash.</span><span class="sxs-lookup"><span data-stu-id="6a676-170">You can create a single hash object and add all of the common data to the hash object.</span></span> <span data-ttu-id="6a676-171">Em seguida, você pode usar a função [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) para criar uma duplicata do objeto de hash original.</span><span class="sxs-lookup"><span data-stu-id="6a676-171">Then, you can use the [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) function to create a duplicate of the original hash object.</span></span> <span data-ttu-id="6a676-172">O objeto hash duplicado contém todas as mesmas informações de estado e dados com hash como o original, mas é um objeto hash completamente independente.</span><span class="sxs-lookup"><span data-stu-id="6a676-172">The duplicate hash object contains all of the same state information and hashed data as the original, but it is a completely independent hash object.</span></span> <span data-ttu-id="6a676-173">Agora você pode adicionar os dados exclusivos a cada um dos objetos de hash e obter o valor de hash, conforme mostrado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="6a676-173">You can now add the unique data to each of the hash objects and obtain the hash value as shown in the example.</span></span> <span data-ttu-id="6a676-174">Essa técnica é útil ao aplicar o hash a uma quantidade possivelmente grande de dados comuns.</span><span class="sxs-lookup"><span data-stu-id="6a676-174">This technique is useful when hashing a possibly large amount of common data.</span></span> <span data-ttu-id="6a676-175">Você só precisa adicionar os dados comuns ao hash original uma vez e, em seguida, pode duplicar o objeto de hash para obter um objeto hash exclusivo.</span><span class="sxs-lookup"><span data-stu-id="6a676-175">You only have to add the common data to the original hash one time, and then you can duplicate the hash object to obtain a unique hash object.</span></span>

 

 
