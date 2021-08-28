---
description: 'API de criptografia: A CNG (Próxima Geração) fornece funções que consultam, adicionam, removem e priorizam os suites de criptografia compatíveis com um provedor. As alterações feitas usando essas funções funcionam imediatamente e não exigem a reinicialização de um servidor ativo.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Priorizando os Schannel Cipher Suites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4436d2f72ebaa1f8d551d935ea9f16d2c03cd7c75fc7d40a73f1a27c7406ad6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920765"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Priorizando os Schannel Cipher Suites

[API de criptografia:](../seccng/cng-portal.md) A CNG (Próxima Geração) fornece funções que consultam, adicionam, removem e priorizam os suites de criptografia compatíveis com um provedor. As alterações feitas usando essas funções funcionam imediatamente e não exigem a reinicialização de um servidor ativo.

> [!Note]
> Você também pode modificar a lista de conjunto de codificação definindo as configurações de política do grupo ordem de criptografia **SSL usando** o snap-in de objeto Política de Grupo no Console de Gerenciamento Microsoft.
> 
> **Para definir a **configuração de política de grupo de pedido do Pacote de Criptografia SSL****
> 
> 1.  Em um prompt de comando, **insira gpedit.msc**. A **Editor de Objeto de Política de Grupo** é exibida.
> 2.  Expanda **Configuração do** **Computador, Modelos Administrativos,** **Redee** clique em **Configuração SSL Configurações**.
> 3.  Em **Configuração SSL Configurações**, clique na configuração Ordem do Conjunto de Criptografia **SSL.**
> 4.  No painel **Ordem do Conjunto de Criptografia SSL,** role até a parte inferior do painel.
> 5.  Siga as instruções rotuladas **Como modificar essa configuração.**
> 
> É necessário reiniciar o computador depois de modificar essa configuração para que as alterações entre em vigor.

 

A lista de conjunto de criptografias é limitada a 1023 caracteres.

Para priorizar os suites de criptografia Schannel, consulte os exemplos a seguir.

-   [Listando os conjunto de criptografias com suporte](#listing-supported-cipher-suites)
-   [Adicionando, removendo e priorizando os cipher suites](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Listando os conjunto de criptografias com suporte

Chame a [**função BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para listar os suites de criptografia que um provedor dá suporte em ordem de prioridade.

O exemplo a seguir demonstra como usar a [**função BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para listar os pacote de criptografia com suporte.


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



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>Adicionando, removendo e priorizando os cipher suites

Chame as funções [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) e [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) para adicionar e remover os suites de criptografia da lista de conjunto de criptografia com suporte.

Ao adicionar um conjunto de criptografias, de definido o valor do parâmetro *dwPosition* da função [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) como **CRYPT PRIORITY \_ \_ TOP** para adicioná-lo à parte superior da lista priorizada ou para **CRYPT PRIORITY \_ \_ BOTTOM** para adicioná-lo à parte inferior da lista.

Para priorizar a lista de conjunto de criptografias, remova todos os conjunto de criptografias da lista e adicione os pacote de criptografia à lista na ordem que você deseja.

O exemplo a seguir mostra como adicionar um conjunto de criptografias à parte superior da lista priorizada para o Provedor Schannel padrão da Microsoft.


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



O exemplo a seguir mostra como remover um conjunto de criptografias da lista priorizada para o Provedor Microsoft Schannel padrão.


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



 

 
