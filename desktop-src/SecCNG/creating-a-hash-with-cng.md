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
# <a name="creating-a-hash-with-cng"></a>Criando um hash com CNG

Um [*hash*](/windows/desktop/SecGloss/h-gly) é uma operação unidirecional que é executada em um bloco de dados para criar um valor de hash exclusivo que representa o conteúdo dos dados. Não importa quando o hash é executado, o mesmo [*algoritmo de hash*](/windows/desktop/SecGloss/h-gly) executado nos mesmos dados sempre produzirá o mesmo valor de hash. Se qualquer um dos dados for alterado, o valor de hash será alterado adequadamente.

Os hashes não são úteis para criptografar dados porque não se destinam a serem usados para reproduzir os dados originais do valor de hash. Os hashes são mais úteis para verificar a integridade dos dados quando usados com um algoritmo de assinatura assimétrica. Por exemplo, se você tiver um hash de uma mensagem de texto, assinado o hash e incluído o valor de hash assinado com a mensagem original, o destinatário poderá verificar o hash assinado, criar o valor de hash da mensagem recebida e comparar esse valor de hash com o valor de hash assinado incluído com a mensagem original. Se os dois valores de hash forem idênticos, o destinatário poderá ser razoavelmente certo de que a mensagem original não foi modificada.

O tamanho do valor de hash é fixo para um algoritmo de hash específico. Isso significa que, independentemente do tamanho do bloco de dados grande ou pequeno, o valor de hash sempre será o mesmo. Por exemplo, o algoritmo de hash SHA256 tem um tamanho de valor de hash de 256 bits.

-   [Criando um objeto de hash](#creating-a-hashing-object)
-   [Criando um objeto de hash reutilizável](#creating-a-reusable-hashing-object)
-   [Duplicando um objeto de hash](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a>Criando um objeto de hash

Para criar um hash usando a CNG, execute as seguintes etapas:

1.  Abra um provedor de algoritmo que dê suporte ao algoritmo desejado. Os algoritmos de hash típicos incluem MD2, MD4, MD5, SHA-1 e SHA256. Chame a função [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e especifique o identificador de algoritmo apropriado no parâmetro *pszAlgId* . A função retorna um identificador para o provedor.
2.  Execute as seguintes etapas para criar o objeto de hash:

    1.  Obtenha o tamanho do objeto chamando a função [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para recuperar a propriedade de **\_ \_ comprimento do objeto BCRYPT** .
    2.  Aloque memória para manter o objeto de hash.
    3.  Crie o objeto chamando a função [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .

3.  Hash dos dados. Isso envolve chamar a função [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) uma ou mais vezes. Cada chamada acrescenta os dados especificados ao hash.
4.  Execute as seguintes etapas para obter o valor de hash:

    1.  Recupere o tamanho do valor chamando a função [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para obter a propriedade de **\_ \_ comprimento de hash BCRYPT** .
    2.  Aloque memória para manter o valor.
    3.  Recupere o valor de hash chamando a função [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) . Depois que essa função for chamada, o objeto hash não será mais válido.

5.  Para concluir este procedimento, você deve executar as seguintes etapas de limpeza:

    1.  Feche o objeto de hash passando o identificador de hash para a função [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Libere a memória alocada para o objeto de hash.
    3.  Se você não estiver criando mais objetos hash, feche o provedor de algoritmos passando o identificador do provedor para a função [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .

        Se você for criar mais objetos de hash, sugerimos que você reutilize o provedor de algoritmo em vez de criar e destruir o mesmo tipo de provedor de algoritmo muitas vezes.

    4.  Quando você terminar de usar a memória de valor de hash, libere-a.

O exemplo a seguir mostra como criar um valor de hash usando a CNG.


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



## <a name="creating-a-reusable-hashing-object"></a>Criando um objeto de hash reutilizável

A partir do Windows 8 e do Windows Server 2012, você pode criar um objeto de hash reutilizável para cenários que exigem a computação de vários hashes ou HMACs em uma rápida sucessão. Faça isso especificando o **sinalizador BCRYPT \_ hash \_ reutilizável \_** ao chamar a função [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) . Todos os provedores de algoritmos de hash da Microsoft dão suporte a esse sinalizador. Um objeto de hash criado com esse sinalizador pode ser reutilizado imediatamente após chamar [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) , como se ele tivesse sido criado de forma nova, chamando [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash). Execute as seguintes etapas para criar um objeto de hash reutilizável:

1.  Abra um provedor de algoritmo que dê suporte ao algoritmo de hash desejado. Chame a função [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e especifique o identificador de algoritmo apropriado no parâmetro *pszAlgId* e **no \_ \_ \_ sinalizador BCRYPT hash reutilizável** no parâmetro *dwFlags* . A função retorna um identificador para o provedor.
2.  Execute as seguintes etapas para criar o objeto de hash:

    1.  Obtenha o tamanho do objeto chamando a função [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para recuperar a propriedade de **\_ \_ comprimento do objeto BCRYPT** .
    2.  Aloque memória para manter o objeto de hash.
    3.  Crie o objeto chamando a função [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Especifique **o \_ \_ \_ sinalizador de hash reutilizável de BCRYPT** no parâmetro *dwFlags* .

3.  Hash dos dados chamando a função [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .
4.  Execute as seguintes etapas para obter o valor de hash:

    1.  Obtenha o tamanho do valor de hash chamando a função [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para obter a propriedade **de \_ \_ comprimento de hash BCRYPT** .
    2.  Aloque memória para manter o valor.
    3.  Obtenha o valor de hash chamando [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).

5.  Para reutilizar o objeto de hash com novos dados, vá para a etapa 3.
6.  Para concluir este procedimento, você deve executar as seguintes etapas de limpeza:

    1.  Feche o objeto de hash passando o identificador de hash para a função [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Libere a memória alocada para o objeto de hash.
    3.  Se você não estiver criando mais objetos hash, feche o provedor de algoritmos passando o identificador do provedor para a função [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .
    4.  Quando você terminar de usar a memória de valor de hash, libere-a.

## <a name="duplicating-a-hash-object"></a>Duplicando um objeto de hash

Em algumas circunstâncias, pode ser útil fazer hash de alguma quantidade de dados comuns e, em seguida, criar dois objetos de hash separados a partir dos dados comuns. Você não precisa criar dois objetos de hash separados e aplicar o hash aos dados comuns duas vezes para fazer isso. Você pode criar um único objeto de hash e adicionar todos os dados comuns ao objeto de hash. Em seguida, você pode usar a função [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) para criar uma duplicata do objeto de hash original. O objeto hash duplicado contém todas as mesmas informações de estado e dados com hash como o original, mas é um objeto hash completamente independente. Agora você pode adicionar os dados exclusivos a cada um dos objetos de hash e obter o valor de hash, conforme mostrado no exemplo. Essa técnica é útil ao aplicar o hash a uma quantidade possivelmente grande de dados comuns. Você só precisa adicionar os dados comuns ao hash original uma vez e, em seguida, pode duplicar o objeto de hash para obter um objeto hash exclusivo.

 

 
