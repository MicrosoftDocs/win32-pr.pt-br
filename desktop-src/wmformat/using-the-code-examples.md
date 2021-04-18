---
title: Usando os exemplos de código do SDK do Windows Media Format
description: Usando os exemplos de código do SDK do Windows Media Format
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- SDK do Windows Media Format, exemplos de código
- SDK do Windows Media Format, código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369179"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a><span data-ttu-id="4c4b9-105">Usando os exemplos de código do SDK do Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="4c4b9-105">Using the Windows Media Format SDK Code Examples</span></span>

<span data-ttu-id="4c4b9-106">Muitas das seções explicativas deste SDK incluem exemplos de código.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-106">Many of the explanatory sections of this SDK include code examples.</span></span> <span data-ttu-id="4c4b9-107">Os exemplos são escritos para serem tão claros e concisos quanto possível.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-107">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="4c4b9-108">Ao ler os exemplos, você deve estar ciente das convenções a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-108">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="4c4b9-109">Todos os exemplos são presumidos para incluir Windows. h e WMSDK. h.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-109">All examples are assumed to include windows.h and wmsdk.h.</span></span> <span data-ttu-id="4c4b9-110">Quaisquer outros arquivos de cabeçalho necessários são mencionados no texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-110">Any other required header files are mentioned in the explanatory text.</span></span>
-   <span data-ttu-id="4c4b9-111">A verificação de erros foi restrita à interrupção da função se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-111">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="4c4b9-112">Em um aplicativo, você deve verificar se há códigos de erro específicos e fornecer algum tipo de relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-112">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>

    <span data-ttu-id="4c4b9-113">Ao verificar valores de retorno de métodos ou funções que retornam um valor **HRESULT** , você deve usar a macro **Failed** para descobrir se o valor de retorno indica falha.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-113">When checking return values from methods or functions that return an **HRESULT** value, you should use the **FAILED** macro to discover whether the return value indicates failure.</span></span>

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    <span data-ttu-id="4c4b9-114">Muitos dos exemplos nesta documentação usam uma macro chamada GOTO \_ Exit \_ If \_ Failed, que é definida no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-114">Many of the examples in this documentation use a macro named GOTO\_EXIT\_IF\_FAILED, which is defined in the following code.</span></span>

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    <span data-ttu-id="4c4b9-115">Essas funções de exemplo têm uma marca chamada "Exit:", após a qual todas as interfaces e memória alocadas na função são liberadas e o código de erro, se houver, é retornado.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-115">These example functions each have a tag named "Exit:", after which all interfaces and memory allocated in the function are released and the error code, if any, is returned.</span></span>

-   <span data-ttu-id="4c4b9-116">Interfaces e memória são liberadas nos exemplos de código usando macros nomeadas de \_ liberação segura e \_ exclusão de matriz segura \_ .</span><span class="sxs-lookup"><span data-stu-id="4c4b9-116">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="4c4b9-117">Essas macros são definidas no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="4c4b9-117">These macros are defined in the following code:</span></span>
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   <span data-ttu-id="4c4b9-118">Geralmente, você precisará incluir a lógica de um exemplo em outro exemplo para que o exemplo seja significativo.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-118">Often, you will need to include the logic of one example in another example for the example to be meaningful.</span></span> <span data-ttu-id="4c4b9-119">Nessas instâncias, um comentário TODO é incluído, com uma referência ao exemplo de código apropriado.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-119">In those instances, a TODO comment is included, with a reference to the appropriate code example.</span></span>
-   <span data-ttu-id="4c4b9-120">Para facilitar a leitura do código, nenhuma das funções de exemplo nesta documentação validam seus parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-120">To make the code easier to read, none of the example functions in this documentation validate their input parameters.</span></span> <span data-ttu-id="4c4b9-121">Se você copiar qualquer uma dessas funções em seu código, deverá validar quaisquer parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c4b9-121">If you copy any of these functions into your code, you should validate any input parameters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c4b9-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c4b9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c4b9-123">**Introdução**</span><span class="sxs-lookup"><span data-stu-id="4c4b9-123">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 




