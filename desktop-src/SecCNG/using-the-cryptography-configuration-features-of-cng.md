---
description: Fornece funções para enumerar e obter informações sobre provedores registrados.
ms.assetid: 5b07060e-0c66-4bf2-b697-05231cb38375
title: Usando os recursos de configuração de criptografia da CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd700b52810f43381722a315bec12216acd7b683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757482"
---
# <a name="using-the-cryptography-configuration-features-of-cng"></a>Usando os recursos de configuração de criptografia da CNG

A API CNG fornece funções para enumerar e obter informações sobre provedores registrados.

-   [Enumerar provedores](#enumerating-providers)
-   [Obtendo informações de registro do provedor](#getting-provider-registration-information)

## <a name="enumerating-providers"></a>Enumerar provedores

Você usa a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para enumerar os provedores registrados. A função **BCryptEnumRegisteredProviders** pode ser chamada de uma das duas maneiras:

1.  A primeira é fazer com que a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) aloque a memória. Isso é feito passando o endereço de um ponteiro **NULL** para o parâmetro *ppBuffer* . Esse código irá alocar a memória necessária para a estrutura de [**\_ provedores cript**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) e as cadeias de caracteres associadas. Quando a função **BCryptEnumRegisteredProviders** é usada dessa maneira, você deve liberar a memória quando ela não for mais necessária passando *ppBuffer* para a função [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .

    O exemplo a seguir mostra como usar a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para alocar o buffer para você.

    ```C++
    #include <windows.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders1()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;
        PCRYPT_PROVIDERS pBuffer = NULL;

        /*
        Get the providers, letting the BCryptEnumRegisteredProviders 
        function allocate the memory.
        */
        status = BCryptEnumRegisteredProviders(&cbBuffer, &pBuffer);

        if (NT_SUCCESS(status))
        {
            if (pBuffer != NULL)
            {
                // Enumerate the providers.
                for (ULONG i = 0; i < pBuffer->cProviders; i++)
                {
                    printf("%S\n", pBuffer->rgpszProviders[i]);
                }
            }
        }
        else
        {
            printf("BCryptEnumRegisteredProviders failed with error " 
                "code 0x%08x\n", status);
        }

        if (NULL != pBuffer)
        {
            /*
            Free the memory allocated by the 
            BCryptEnumRegisteredProviders function.
            */
            BCryptFreeBuffer(pBuffer);
        }
    }
    
    ```

    

2.  O segundo método é alocar a memória necessária por conta própria. Isso é feito chamando a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) com **NULL** para o parâmetro *ppBuffer* . A função **BCryptEnumRegisteredProviders** será colocada no valor apontado pelo parâmetro *pcbBuffer* , o tamanho necessário, em bytes, da estrutura de [**\_ provedores cript**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) e de todas as cadeias de caracteres. Em seguida, você aloca a memória necessária e passa o endereço desse ponteiro de buffer para o parâmetro *ppBuffer* em uma segunda chamada para a função **BCryptEnumRegisteredProviders** .

    O exemplo a seguir mostra como usar a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para alocar e usar seu próprio buffer.

    ```C++
    #include <windows.h>
    #include <stdio.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders2()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;

        // Get the required size of the buffer.
        status = BCryptEnumRegisteredProviders(&cbBuffer, NULL);

        if (STATUS_BUFFER_TOO_SMALL == status)
        {
            // Allocate the buffer.
            PCRYPT_PROVIDERS pBuffer = 
                (PCRYPT_PROVIDERS)LocalAlloc(LPTR, cbBuffer);
            if (NULL != pBuffer)
            {
                // Get the providers in the buffer that was allocated.
                status = BCryptEnumRegisteredProviders(
                    &cbBuffer, 
                    &pBuffer);
                if (NT_SUCCESS(status))
                {
                    for (ULONG i = 0; i < pBuffer->cProviders; i++)
                    {
                        // Enumerate the providers.
                        printf("%S\n", pBuffer->rgpszProviders[i]);
                    }
                }

                // Free the memory that was allocated.
                LocalFree(pBuffer);
            }
        }
    }
    
    ```

    

## <a name="getting-provider-registration-information"></a>Obtendo informações de registro do provedor

A função [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) é usada para obter informações adicionais específicas de registro sobre um provedor. Essa função usa o nome do provedor para o qual você deseja obter informações, o modo de provedor desejado (modo kernel, modo de usuário ou ambos) e o identificador da interface do provedor para recuperar as informações de registro. Por exemplo, para obter as informações de registro do modo de usuário para a interface de codificação para o provedor "Microsoft Primitive Provider", você fará uma chamada semelhante à seguinte.


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



Assim como a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , a função [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) pode alocar memória para você ou pode alocar a memória por conta própria. O processo é o mesmo para as duas funções.

 

 



