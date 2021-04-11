---
description: 'Cryptography API: próxima geração (CNG) fornece funções que consultam, adicionam, removem e priorizam os conjuntos de codificação aos quais um provedor dá suporte. As alterações feitas usando essas funções entram em vigor imediatamente e não exigem a reinicialização de um servidor ativo.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Priorizando conjuntos de codificação Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f885c4d51006233be252a02c7cc3bebd26a4e6c3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172559"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Priorizando conjuntos de codificação Schannel

[CRYPTOGRAPHY API: próxima geração](../seccng/cng-portal.md) (CNG) fornece funções que consultam, adicionam, removem e priorizam os conjuntos de codificação aos quais um provedor dá suporte. As alterações feitas usando essas funções entram em vigor imediatamente e não exigem a reinicialização de um servidor ativo.

> [!Note]
> Você também pode modificar a lista de conjuntos de codificação configurando as configurações da política de grupo do **conjunto de codificação SSL** usando o snap-in de objeto política de grupo no console de gerenciamento Microsoft.
> 
> **Para definir a configuração da política de grupo **SSL Cipher Suite Order****
> 
> 1.  Em um prompt de comando, digite **gpedit. msc**. O **Editor de objeto de política de grupo** é exibido.
> 2.  Expanda **configuração do computador**, **modelos administrativos**, **rede** e clique em definições de **configuração de SSL**.
> 3.  Em **definições de configuração de SSL**, clique na configuração de **ordem do conjunto de codificação SSL** .
> 4.  No painel **ordem do conjunto de criptografia SSL** , role até a parte inferior do painel.
> 5.  Siga as instruções rotuladas **como modificar essa configuração**.
> 
> É necessário reiniciar o computador depois de modificar essa configuração para que as alterações entrem em vigor.

 

A lista de conjuntos de codificação é limitada a 1023 caracteres.

Para priorizar os conjuntos de codificação Schannel, consulte os exemplos a seguir.

-   [Listando conjuntos de codificação com suporte](#listing-supported-cipher-suites)
-   [Adicionando, removendo e priorizando conjuntos de codificação](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Listando conjuntos de codificação com suporte

Chame a função [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para listar os conjuntos de codificação que um provedor suporta em ordem de prioridade.

O exemplo a seguir demonstra como usar a função [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para listar os conjuntos de criptografia com suporte.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{

   HRESULT Status = ERROR_SUCCESS;
   DWORD   cbBuffer = 0;
   PCRYPT_CONTEXT_FUNCTIONS pBuffer = NULL;

    Status = BCryptEnumContextFunctions(
        CRYPT_LOCAL,
        L"SSL",
        NCRYPT_SCHANNEL_INTERFACE,
        &cbBuffer,
        &pBuffer);
    if(FAILED(Status))
    {
        printf_s("\n**** Error 0x%x returned by BCryptEnumContextFunctions\n", Status);
        goto Cleanup;
    }
                
    if(pBuffer == NULL)
    {
        printf_s("\n**** Error pBuffer returned from BCryptEnumContextFunctions is null");
        goto Cleanup;
    }

    printf_s("\n\n Listing Cipher Suites ");
    for(UINT index = 0; index < pBuffer->cFunctions; ++index)
    {
        printf_s("\n%S", pBuffer->rgpszFunctions[index]);
    }

Cleanup:
    if (pBuffer != NULL)
    {
        BCryptFreeBuffer(pBuffer);
    }
}


```



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>Adicionando, removendo e priorizando conjuntos de codificação

Chame as funções [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) e [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) para adicionar e remover conjuntos de codificação da lista de conjuntos de codificação com suporte.

Ao adicionar um conjunto de codificação, defina o valor do parâmetro *dwPosition* da função [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) para a **\_ \_ parte superior de cript** . para adicioná-lo à parte superior da lista de prioridades ou **à \_ \_ parte inferior da prioridade criptografada** para adicioná-lo à parte inferior da lista.

Para priorizar a lista de conjuntos de codificação, remova todos os conjuntos de codificação da lista e, em seguida, adicione pacotes de codificação à lista na ordem desejada.

O exemplo a seguir mostra como adicionar um conjunto de codificação na parte superior da lista de prioridades para o provedor padrão do Microsoft Schannel.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
    LPWSTR wszCipher = (L"RSA_EXPORT1024_DES_CBC_SHA");
       
    Status = BCryptAddContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher,
                CRYPT_PRIORITY_TOP);
}


```



O exemplo a seguir mostra como remover um conjunto de codificação da lista de prioridades para o provedor padrão do Microsoft Schannel.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
      LPWSTR wszCipher = (L"TLS_RSA_WITH_RC4_128_SHA");
       
    Status = BCryptRemoveContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher);
}


```



 

 
