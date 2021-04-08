---
description: Ao chamar os entryPoints de um assembly, é recomendável que você use o mesmo contexto de ativação que estava ativo ao pesquisar o assembly.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Chamando assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921953"
---
# <a name="calling-into-assemblies"></a><span data-ttu-id="e8d4c-103">Chamando assemblies</span><span class="sxs-lookup"><span data-stu-id="e8d4c-103">Calling Into Assemblies</span></span>

<span data-ttu-id="e8d4c-104">Ao chamar os entryPoints de um assembly, é recomendável que você use o mesmo contexto de ativação que estava ativo ao pesquisar o assembly.</span><span class="sxs-lookup"><span data-stu-id="e8d4c-104">When calling into the entrypoints of an assembly, it is recommended that you use the same activation context that was active when searching for the assembly.</span></span> <span data-ttu-id="e8d4c-105">No mínimo, verifique se o componente que está carregando o assembly não obtém acidentalmente o contexto de ativação que seu aplicativo está usando.</span><span class="sxs-lookup"><span data-stu-id="e8d4c-105">At minimum, ensure that the component loading the assembly does not accidentally get the activation context your application is using.</span></span> <span data-ttu-id="e8d4c-106">O vazamento do contexto de ativação entre limites de DLL pode levar a dependências inesperadas.</span><span class="sxs-lookup"><span data-stu-id="e8d4c-106">Leaking activation context across DLL boundaries can lead to unexpected dependencies.</span></span> <span data-ttu-id="e8d4c-107">Isso não é um problema se o aplicativo compilar o reconhecimento de \_ isolamento \_ habilitado porque, nesse caso, nenhum contexto de ativação está ativo por padrão.</span><span class="sxs-lookup"><span data-stu-id="e8d4c-107">This is not a problem if your application compiles ISOLATION\_AWARE\_ENABLED because in that case no activation context is active by default.</span></span> <span data-ttu-id="e8d4c-108">Se você não compilar com reconhecimento de \_ isolamento \_ habilitado definido, deverá ativar o contexto de ativação **NULL** ou o mesmo contexto de ativação que foi usado para carregar o assembly.</span><span class="sxs-lookup"><span data-stu-id="e8d4c-108">If you do not compile with ISOLATION\_AWARE\_ENABLED defined, you should activate the **NULL** activation context or the same activation context that was used to load the assembly.</span></span>

<span data-ttu-id="e8d4c-109">O exemplo a seguir garante que a DLL hospedada seja executada em um contexto que ela reconheça:</span><span class="sxs-lookup"><span data-stu-id="e8d4c-109">The following example ensures that the hosted DLL runs in a context that it recognizes:</span></span>

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



