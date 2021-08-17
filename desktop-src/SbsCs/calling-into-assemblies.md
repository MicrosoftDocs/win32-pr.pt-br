---
description: Ao chamar para os pontos de entrada de um assembly, é recomendável usar o mesmo contexto de ativação que estava ativo ao pesquisar o assembly.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Chamando em assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6f785c9d68aa0dbf4bec24927d9f2a1443aed1fb7fe65ec9244616fce8feec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142419"
---
# <a name="calling-into-assemblies"></a>Chamando em assemblies

Ao chamar para os pontos de entrada de um assembly, é recomendável usar o mesmo contexto de ativação que estava ativo ao pesquisar o assembly. No mínimo, verifique se o componente que carrega o assembly não tem acidentalmente o contexto de ativação que seu aplicativo está usando. O vazamento do contexto de ativação entre limites de DLL pode levar a dependências inesperadas. Isso não será um problema se o aplicativo compilar ISOLATION AWARE ENABLED porque, nesse caso, nenhum contexto de ativação \_ \_ está ativo por padrão. Se você não compilar com ISOLATION AWARE ENABLED definido, deverá ativar o contexto de ativação NULL ou o mesmo contexto de ativação usado para \_ \_ carregar o assembly. 

O exemplo a seguir garante que a DLL hospedada seja executado em um contexto que reconhece:

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

 

 



