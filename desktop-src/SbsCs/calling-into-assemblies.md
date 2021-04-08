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
# <a name="calling-into-assemblies"></a>Chamando assemblies

Ao chamar os entryPoints de um assembly, é recomendável que você use o mesmo contexto de ativação que estava ativo ao pesquisar o assembly. No mínimo, verifique se o componente que está carregando o assembly não obtém acidentalmente o contexto de ativação que seu aplicativo está usando. O vazamento do contexto de ativação entre limites de DLL pode levar a dependências inesperadas. Isso não é um problema se o aplicativo compilar o reconhecimento de \_ isolamento \_ habilitado porque, nesse caso, nenhum contexto de ativação está ativo por padrão. Se você não compilar com reconhecimento de \_ isolamento \_ habilitado definido, deverá ativar o contexto de ativação **NULL** ou o mesmo contexto de ativação que foi usado para carregar o assembly.

O exemplo a seguir garante que a DLL hospedada seja executada em um contexto que ela reconheça:

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

 

 



