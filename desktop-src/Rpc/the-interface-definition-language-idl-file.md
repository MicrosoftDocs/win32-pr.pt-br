---
title: O arquivo IDL (Interface Definition Language)
description: Um arquivo IDL contém uma ou mais definições de interface.
ms.assetid: ca01766d-ec7f-4906-9927-0835aeda4981
keywords:
- RPC de arquivos IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53859d138528b4096cc99912be1ca0f59317c674
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008079"
---
# <a name="the-interface-definition-language-idl-file"></a><span data-ttu-id="a0223-104">O arquivo IDL (Interface Definition Language)</span><span class="sxs-lookup"><span data-stu-id="a0223-104">The Interface Definition Language (IDL) File</span></span>

<span data-ttu-id="a0223-105">Um arquivo IDL contém uma ou mais definições de interface.</span><span class="sxs-lookup"><span data-stu-id="a0223-105">An IDL file contains one or more interface definitions.</span></span> <span data-ttu-id="a0223-106">Cada definição de interface é composta por um cabeçalho de interface e um corpo de interface.</span><span class="sxs-lookup"><span data-stu-id="a0223-106">Each interface definition is composed of an interface header and an interface body.</span></span> <span data-ttu-id="a0223-107">O cabeçalho da interface é demarcadas por colchetes.</span><span class="sxs-lookup"><span data-stu-id="a0223-107">The interface header is demarcated by square brackets.</span></span> <span data-ttu-id="a0223-108">O corpo da interface está entre chaves.</span><span class="sxs-lookup"><span data-stu-id="a0223-108">The interface body is contained in curly brackets.</span></span> <span data-ttu-id="a0223-109">Isso é ilustrado na seguinte interface de exemplo:</span><span class="sxs-lookup"><span data-stu-id="a0223-109">This is illustrated in the following example interface:</span></span>

``` syntax
[
  /*Interface attributes go here. */
]
interface INTERFACENAME
{
  /*The interface body goes here. */
}
```

<span data-ttu-id="a0223-110">Esta seção fornece uma visão geral dos componentes de uma interface.</span><span class="sxs-lookup"><span data-stu-id="a0223-110">This section gives an overview of the components of an interface.</span></span> <span data-ttu-id="a0223-111">Ele é organizado nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a0223-111">It is organized into the following topics:</span></span>

-   [<span data-ttu-id="a0223-112">O cabeçalho da interface IDL</span><span class="sxs-lookup"><span data-stu-id="a0223-112">The IDL Interface Header</span></span>](the-idl-interface-header.md)
-   [<span data-ttu-id="a0223-113">O corpo da interface IDL</span><span class="sxs-lookup"><span data-stu-id="a0223-113">The IDL Interface Body</span></span>](the-idl-interface-body.md)

## <a name="related-topics"></a><span data-ttu-id="a0223-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0223-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0223-115">Atributos IDL</span><span class="sxs-lookup"><span data-stu-id="a0223-115">IDL Attributes</span></span>](/windows/desktop/Midl/idl-attributes)
</dt> </dl>

 

 