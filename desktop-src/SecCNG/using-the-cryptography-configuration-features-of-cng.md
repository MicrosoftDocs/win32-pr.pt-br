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
# <a name="using-the-cryptography-configuration-features-of-cng"></a><span data-ttu-id="85173-103">Usando os recursos de configuração de criptografia da CNG</span><span class="sxs-lookup"><span data-stu-id="85173-103">Using the Cryptography Configuration Features of CNG</span></span>

<span data-ttu-id="85173-104">A API CNG fornece funções para enumerar e obter informações sobre provedores registrados.</span><span class="sxs-lookup"><span data-stu-id="85173-104">The CNG API provides functions to enumerate and obtain information about registered providers.</span></span>

-   [<span data-ttu-id="85173-105">Enumerar provedores</span><span class="sxs-lookup"><span data-stu-id="85173-105">Enumerating Providers</span></span>](#enumerating-providers)
-   [<span data-ttu-id="85173-106">Obtendo informações de registro do provedor</span><span class="sxs-lookup"><span data-stu-id="85173-106">Getting Provider Registration Information</span></span>](#getting-provider-registration-information)

## <a name="enumerating-providers"></a><span data-ttu-id="85173-107">Enumerar provedores</span><span class="sxs-lookup"><span data-stu-id="85173-107">Enumerating Providers</span></span>

<span data-ttu-id="85173-108">Você usa a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para enumerar os provedores registrados.</span><span class="sxs-lookup"><span data-stu-id="85173-108">You use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to enumerate the registered providers.</span></span> <span data-ttu-id="85173-109">A função **BCryptEnumRegisteredProviders** pode ser chamada de uma das duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="85173-109">The **BCryptEnumRegisteredProviders** function can be called in one of two ways:</span></span>

1.  <span data-ttu-id="85173-110">A primeira é fazer com que a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) aloque a memória.</span><span class="sxs-lookup"><span data-stu-id="85173-110">The first is to have the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function allocate the memory.</span></span> <span data-ttu-id="85173-111">Isso é feito passando o endereço de um ponteiro **NULL** para o parâmetro *ppBuffer* .</span><span class="sxs-lookup"><span data-stu-id="85173-111">This is accomplished by passing the address of a **NULL** pointer for the *ppBuffer* parameter.</span></span> <span data-ttu-id="85173-112">Esse código irá alocar a memória necessária para a estrutura de [**\_ provedores cript**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) e as cadeias de caracteres associadas.</span><span class="sxs-lookup"><span data-stu-id="85173-112">This code will allocate the memory required for the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and the associated strings.</span></span> <span data-ttu-id="85173-113">Quando a função **BCryptEnumRegisteredProviders** é usada dessa maneira, você deve liberar a memória quando ela não for mais necessária passando *ppBuffer* para a função [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .</span><span class="sxs-lookup"><span data-stu-id="85173-113">When the **BCryptEnumRegisteredProviders** function is used in this manner, you must free the memory when it is no longer needed by passing *ppBuffer* to the [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) function.</span></span>

    <span data-ttu-id="85173-114">O exemplo a seguir mostra como usar a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para alocar o buffer para você.</span><span class="sxs-lookup"><span data-stu-id="85173-114">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate the buffer for you.</span></span>

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

    

2.  <span data-ttu-id="85173-115">O segundo método é alocar a memória necessária por conta própria.</span><span class="sxs-lookup"><span data-stu-id="85173-115">The second method is to allocate the required memory yourself.</span></span> <span data-ttu-id="85173-116">Isso é feito chamando a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) com **NULL** para o parâmetro *ppBuffer* .</span><span class="sxs-lookup"><span data-stu-id="85173-116">This is accomplished by calling the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function with **NULL** for the *ppBuffer* parameter.</span></span> <span data-ttu-id="85173-117">A função **BCryptEnumRegisteredProviders** será colocada no valor apontado pelo parâmetro *pcbBuffer* , o tamanho necessário, em bytes, da estrutura de [**\_ provedores cript**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) e de todas as cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="85173-117">The **BCryptEnumRegisteredProviders** function will place in the value pointed to by the *pcbBuffer* parameter, the required size, in bytes, of the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and all strings.</span></span> <span data-ttu-id="85173-118">Em seguida, você aloca a memória necessária e passa o endereço desse ponteiro de buffer para o parâmetro *ppBuffer* em uma segunda chamada para a função **BCryptEnumRegisteredProviders** .</span><span class="sxs-lookup"><span data-stu-id="85173-118">You then allocate the required memory and pass the address of this buffer pointer for the *ppBuffer* parameter in a second call to the **BCryptEnumRegisteredProviders** function.</span></span>

    <span data-ttu-id="85173-119">O exemplo a seguir mostra como usar a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para alocar e usar seu próprio buffer.</span><span class="sxs-lookup"><span data-stu-id="85173-119">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate and use your own buffer.</span></span>

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

    

## <a name="getting-provider-registration-information"></a><span data-ttu-id="85173-120">Obtendo informações de registro do provedor</span><span class="sxs-lookup"><span data-stu-id="85173-120">Getting Provider Registration Information</span></span>

<span data-ttu-id="85173-121">A função [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) é usada para obter informações adicionais específicas de registro sobre um provedor.</span><span class="sxs-lookup"><span data-stu-id="85173-121">The [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function is used to obtain additional, registration-specific information about a provider.</span></span> <span data-ttu-id="85173-122">Essa função usa o nome do provedor para o qual você deseja obter informações, o modo de provedor desejado (modo kernel, modo de usuário ou ambos) e o identificador da interface do provedor para recuperar as informações de registro.</span><span class="sxs-lookup"><span data-stu-id="85173-122">This function takes the name of the provider that you want to obtain information for, the desired provider mode (kernel mode, user mode, or both), and the identifier of the provider interface to retrieve the registration information for.</span></span> <span data-ttu-id="85173-123">Por exemplo, para obter as informações de registro do modo de usuário para a interface de codificação para o provedor "Microsoft Primitive Provider", você fará uma chamada semelhante à seguinte.</span><span class="sxs-lookup"><span data-stu-id="85173-123">For example, to obtain the user mode registration information for the cipher interface for the "Microsoft Primitive Provider" provider, you would make a call similar to the following.</span></span>


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



<span data-ttu-id="85173-124">Assim como a função [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , a função [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) pode alocar memória para você ou pode alocar a memória por conta própria.</span><span class="sxs-lookup"><span data-stu-id="85173-124">Like the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function, the [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function can either allocate memory for you or you can allocate the memory yourself.</span></span> <span data-ttu-id="85173-125">O processo é o mesmo para as duas funções.</span><span class="sxs-lookup"><span data-stu-id="85173-125">The process is the same for the two functions.</span></span>

 

 



