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
# <a name="prioritizing-schannel-cipher-suites"></a><span data-ttu-id="ec5d6-104">Priorizando conjuntos de codificação Schannel</span><span class="sxs-lookup"><span data-stu-id="ec5d6-104">Prioritizing Schannel Cipher Suites</span></span>

<span data-ttu-id="ec5d6-105">[CRYPTOGRAPHY API: próxima geração](../seccng/cng-portal.md) (CNG) fornece funções que consultam, adicionam, removem e priorizam os conjuntos de codificação aos quais um provedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) provides functions that query, add, remove, and prioritize the cipher suites that a provider supports.</span></span> <span data-ttu-id="ec5d6-106">As alterações feitas usando essas funções entram em vigor imediatamente e não exigem a reinicialização de um servidor ativo.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-106">Changes made by using these functions take effect immediately and do not require restarting an active server.</span></span>

> [!Note]
> <span data-ttu-id="ec5d6-107">Você também pode modificar a lista de conjuntos de codificação configurando as configurações da política de grupo do **conjunto de codificação SSL** usando o snap-in de objeto política de grupo no console de gerenciamento Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-107">You can also modify the list of cipher suites by configuring the **SSL Cipher Suite Order** group policy settings using the Group Policy Object snap-in in Microsoft Management Console.</span></span>
> 
> <span data-ttu-id="ec5d6-108">\*\*Para definir a configuração da política de grupo \*\*SSL Cipher Suite Order\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ec5d6-108">**To configure the **SSL Cipher Suite Order** group policy setting**</span></span>
> 
> 1.  <span data-ttu-id="ec5d6-109">Em um prompt de comando, digite **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-109">At a command prompt, enter **gpedit.msc**.</span></span> <span data-ttu-id="ec5d6-110">O **Editor de objeto de política de grupo** é exibido.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-110">The **Group Policy Object Editor** appears.</span></span>
> 2.  <span data-ttu-id="ec5d6-111">Expanda **configuração do computador**, **modelos administrativos**, **rede** e clique em definições de **configuração de SSL**.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-111">Expand **Computer Configuration**, **Administrative Templates**, **Network**, and then click **SSL Configuration Settings**.</span></span>
> 3.  <span data-ttu-id="ec5d6-112">Em **definições de configuração de SSL**, clique na configuração de **ordem do conjunto de codificação SSL** .</span><span class="sxs-lookup"><span data-stu-id="ec5d6-112">Under **SSL Configuration Settings**, click the **SSL Cipher Suite Order** setting.</span></span>
> 4.  <span data-ttu-id="ec5d6-113">No painel **ordem do conjunto de criptografia SSL** , role até a parte inferior do painel.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-113">In the **SSL Cipher Suite Order** pane, scroll to the bottom of the pane.</span></span>
> 5.  <span data-ttu-id="ec5d6-114">Siga as instruções rotuladas **como modificar essa configuração**.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-114">Follow the instructions labeled **How to modify this setting**.</span></span>
> 
> <span data-ttu-id="ec5d6-115">É necessário reiniciar o computador depois de modificar essa configuração para que as alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-115">It is necessary to restart the computer after modifying this setting for the changes to take effect.</span></span>

 

<span data-ttu-id="ec5d6-116">A lista de conjuntos de codificação é limitada a 1023 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-116">The list of cipher suites is limited to 1023 characters.</span></span>

<span data-ttu-id="ec5d6-117">Para priorizar os conjuntos de codificação Schannel, consulte os exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-117">To prioritize Schannel cipher suites, see the following examples.</span></span>

-   [<span data-ttu-id="ec5d6-118">Listando conjuntos de codificação com suporte</span><span class="sxs-lookup"><span data-stu-id="ec5d6-118">Listing Supported Cipher Suites</span></span>](#listing-supported-cipher-suites)
-   [<span data-ttu-id="ec5d6-119">Adicionando, removendo e priorizando conjuntos de codificação</span><span class="sxs-lookup"><span data-stu-id="ec5d6-119">Adding, Removing, and Prioritizing Cipher Suites</span></span>](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a><span data-ttu-id="ec5d6-120">Listando conjuntos de codificação com suporte</span><span class="sxs-lookup"><span data-stu-id="ec5d6-120">Listing Supported Cipher Suites</span></span>

<span data-ttu-id="ec5d6-121">Chame a função [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para listar os conjuntos de codificação que um provedor suporta em ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-121">Call the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list the cipher suites that a provider supports in order of priority.</span></span>

<span data-ttu-id="ec5d6-122">O exemplo a seguir demonstra como usar a função [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para listar os conjuntos de criptografia com suporte.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-122">The following example demonstrates how to use the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list supported cipher suites.</span></span>


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



## <a name="adding-removing-and-prioritizing-cipher-suites"></a><span data-ttu-id="ec5d6-123">Adicionando, removendo e priorizando conjuntos de codificação</span><span class="sxs-lookup"><span data-stu-id="ec5d6-123">Adding, Removing, and Prioritizing Cipher Suites</span></span>

<span data-ttu-id="ec5d6-124">Chame as funções [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) e [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) para adicionar e remover conjuntos de codificação da lista de conjuntos de codificação com suporte.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-124">Call the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) and [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) functions to add and remove cipher suites from the list of supported cipher suites.</span></span>

<span data-ttu-id="ec5d6-125">Ao adicionar um conjunto de codificação, defina o valor do parâmetro *dwPosition* da função [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) para a **\_ \_ parte superior de cript** . para adicioná-lo à parte superior da lista de prioridades ou **à \_ \_ parte inferior da prioridade criptografada** para adicioná-lo à parte inferior da lista.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-125">When adding a cipher suite, set the value of the *dwPosition* parameter of the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) function to **CRYPT\_PRIORITY\_TOP** to add it to the top of the prioritized list, or to **CRYPT\_PRIORITY\_BOTTOM** to add it to the bottom of the list.</span></span>

<span data-ttu-id="ec5d6-126">Para priorizar a lista de conjuntos de codificação, remova todos os conjuntos de codificação da lista e, em seguida, adicione pacotes de codificação à lista na ordem desejada.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-126">To prioritize the list of cipher suites, remove all of the cipher suites from the list, and then add cipher suites to the list in the order you want them.</span></span>

<span data-ttu-id="ec5d6-127">O exemplo a seguir mostra como adicionar um conjunto de codificação na parte superior da lista de prioridades para o provedor padrão do Microsoft Schannel.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-127">The following example shows how to add a cipher suite to the top of the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



<span data-ttu-id="ec5d6-128">O exemplo a seguir mostra como remover um conjunto de codificação da lista de prioridades para o provedor padrão do Microsoft Schannel.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-128">The following example shows how to remove a cipher suite from the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



 

 
