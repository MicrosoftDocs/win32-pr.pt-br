---
title: Usando os exemplos de código do cliente Microsoft Windows Media DRM
description: Usando os exemplos de código do cliente Microsoft Windows Media DRM
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- SDK do Windows Media Format, exemplos de código
- SDK do Windows Media Format, código de exemplo
- SDK do Windows Media Format, exemplos de código DRM
- DRM (gerenciamento de direitos digitais), exemplos de código
- DRM (gerenciamento de direitos digitais), exemplos de código
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054d1ed804873c8aca104203ee1f235ecb3856f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369059"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a><span data-ttu-id="e1b74-110">Usando os exemplos de código do cliente Microsoft Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="e1b74-110">Using the Microsoft Windows Media DRM Client Code Examples</span></span>

<span data-ttu-id="e1b74-111">Os exemplos de código estão incluídos nesta documentação para ilustrar o uso de componentes.</span><span class="sxs-lookup"><span data-stu-id="e1b74-111">Code examples are included in this documentation to illustrate the use of components.</span></span> <span data-ttu-id="e1b74-112">Os exemplos são escritos para serem tão claros e concisos quanto possível.</span><span class="sxs-lookup"><span data-stu-id="e1b74-112">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="e1b74-113">Ao ler os exemplos, você deve estar ciente das convenções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1b74-113">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="e1b74-114">Todos os exemplos são presumidos para incluir Windows. h e wmdrmsdk. h.</span><span class="sxs-lookup"><span data-stu-id="e1b74-114">All examples are assumed to include windows.h and wmdrmsdk.h.</span></span> <span data-ttu-id="e1b74-115">O exemplo incluirá uma observação se precisar de outros cabeçalhos para compilar.</span><span class="sxs-lookup"><span data-stu-id="e1b74-115">The example will include a note if it requires other headers in order to compile.</span></span>
-   <span data-ttu-id="e1b74-116">A verificação de erros foi restrita à interrupção da função se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="e1b74-116">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="e1b74-117">Em um aplicativo, você deve verificar se há códigos de erro específicos e fornecer algum tipo de relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="e1b74-117">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>
-   <span data-ttu-id="e1b74-118">Interfaces e memória são liberadas nos exemplos de código usando macros nomeadas de \_ liberação segura e \_ exclusão de matriz segura \_ .</span><span class="sxs-lookup"><span data-stu-id="e1b74-118">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="e1b74-119">Essas macros são definidas no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="e1b74-119">These macros are defined in the following code:</span></span>
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

    

## <a name="related-topics"></a><span data-ttu-id="e1b74-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1b74-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1b74-121">**Introdução**</span><span class="sxs-lookup"><span data-stu-id="e1b74-121">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




