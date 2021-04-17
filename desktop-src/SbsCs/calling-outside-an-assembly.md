---
description: Chamando fora de um assembly
ms.assetid: 7a59f707-fb89-4899-891f-4cd556b62b26
title: Chamando fora de um assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed60536c3daa62957929dd1d3f1a850fd551ae9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748555"
---
# <a name="calling-outside-an-assembly"></a>Chamando fora de um assembly

Os componentes hospedados devem garantir que o contexto de ativação correto esteja ativo ao chamar fora do componente. Chamadas para o código externo que foi encontrado chamando [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) e, em seguida, [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), devem ser chamadas com o mesmo contexto que foi usado para encontrá-lo. Chamadas para o código que foi encontrado fora dos contextos de ativação ou chamadas de volta para o aplicativo de hospedagem devem ser chamadas com o contexto de ativação padrão do aplicativo.

A compilação com \_ reconhecimento \_ de isolamento habilitado pode ser útil ao chamar fora de componentes hospedados. No entanto, isso significa que somente as chamadas para APIs do Windows são isoladas para o contexto de ativação do componente. Isso é suficiente para a maioria dos casos porque as chamadas para funções de terceiros não têm um contexto ativado antes de serem chamadas. A compilação com \_ habilitado para isolamento \_ definido não ajuda se o seu componente usa vários contextos de ativação com várias APIs de plataforma.

Para implementar isso, use um ativador de contexto de ativação como o exemplo apresentado em [isolando componentes](isolating-components.md). Aqui estão as externas. o manifesto é o conjunto de dependências fora dos quais o componente foi criado; Talvez ele contenha uma lista extensível de componentes que devem ser carregados e usados durante o tempo de execução. O internalcontext. manifest contém o conjunto de dependências que o componente usa durante seu tempo de vida e que deve ser definido em todos os entryPoints de fora. Observe que esse contexto interno é ativado em todos os entryPoints, enquanto o ativador de contexto é usado com o escopo do C++ para que o contexto apropriado seja definido ao chamar os vários códigos externos que esse componente usa.

``` syntax
CActivationContext s_InternalContext;
CActivationContext s_OutboundContext;
CActivationContext s_ExternalContext;

void MyInitializeFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};

    s_OutboundContext.Set(NULL);

    actctx.lpSource = TEXT("internalcontext.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_InternalActCtx.Set(hActCtx);
    ReleaseActCtx(hActCtx);

    actctx.lpSource = TEXT("externals.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_ExternalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
}

void foo() 
{
    // Some code that makes a few calls
    {
        CActCtxActivator CallUnknown(s_OutboundContext);
        pfnUnknownImplementor(...);
    }
    {
        CActCtxActivator CallDependency(s_ExternalContext);
        KnownExternalDependencyPtr->Call();
    }
}

void WINAPI MyEntrypoint() 
{
    CActCtxActivator ContextFirewall(s_InternalContext);
    // Do some work here
    foo();
    // Some more work here
}
```

 

 
