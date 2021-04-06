---
description: Os componentes bem autorizados não perturbarm o ambiente do aplicativo de hospedagem, nem vazam contextos de ativação.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Isolando componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e201375f50324209380a4ecef5fa762ae70e56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826999"
---
# <a name="isolating-components"></a>Isolando componentes

Os componentes bem autorizados não perturbarm o ambiente do aplicativo de hospedagem, nem vazam contextos de ativação. Os componentes bem autorizados executam seu próprio gerenciamento de contexto em vez de depender do ambiente do aplicativo de hospedagem.

O autor do componente hospedado está na melhor posição para saber exatamente quais outros assemblies o componente requer. Depender do aplicativo host para fornecer o ambiente correto para seu componente hospedado é uma provável fonte de erros. Em vez disso, crie um manifesto para seu componente hospedado que especifique todas as suas dependências e, em seguida, compile usando o reconhecimento de isolamento \_ \_ habilitado. Isso garante que as chamadas externas feitas por seu componente sejam isoladas e usem as versões corretas. Como o contexto de ativação \_ \_ habilitado para isolamento usa o é por dll, é seguro usá-lo em várias DLLs, cada um com seu próprio manifesto chamando dependências.

Se não for possível compilar com \_ reconhecimento \_ de isolamento habilitado, use uma solução como a apresentada em [usando retornos de chamada de componentes hospedados](using-callbacks-from-hosted-components.md).

Você deve ativar seu próprio contexto de ativação em todos os pontos de entrada que o aplicativo de hospedagem pode chamar para garantir que seu componente hospedado seja executado inteiramente com o contexto de ativação correto. Você pode usar um objeto auxiliar do C++ para facilitar a alteração de todos os entryPoints. Por exemplo, você pode usar uma classe C++, como a seguinte:


```C++
#include <windows.h>

class CActivationContext 
{
    HANDLE m_hActivationContext;

public:
    CActivationContext() : m_hActivationContext(INVALID_HANDLE_VALUE) 
    {
    }

    VOID Set(HANDLE hActCtx) 
    {
        if (hActCtx != INVALID_HANDLE_VALUE)
            AddRefActCtx(hActCtx);

        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
        m_hActivationContext = hActCtx;
    }

    ~CActivationContext() 
    {
        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
    }

    BOOL Activate(ULONG_PTR &ulpCookie) 
    {
        return ActivateActCtx(m_hActivationContext, &ulpCookie);
    }

    BOOL Deactivate(ULONG_PTR ulpCookie) 
    {
        return DeactivateActCtx(0, ulpCookie);
    }
};

class CActCtxActivator 
{
    CActivationContext &m_ActCtx;
    ULONG_PTR m_Cookie;
    bool m_fActivated;

public:
    CActCtxActivator(CActivationContext& src, bool fActivate = true) 
        : m_ActCtx(src), m_Cookie(0), m_fActivated(false) 
    {
        if (fActivate) {
            if (src.Activate(m_Cookie))
                m_fActivated = true;
        }
    }

    ~CActCtxActivator() 
    {
        if (m_fActivated) {
            m_ActCtx.Deactivate(m_Cookie);
            m_fActivated = false;
        }
    }
};

```



Isso pode ser usado em seu componente, usando uma variável global para armazenar o contexto de ativação que deve ser ativado em cada ponto de entrada. Dessa forma, você pode isolar o componente do seu aplicativo de hospedagem.


```C++
CActivationContext s_GlobalContext;

void MyExportedEntrypoint(void) 
{
    CActCtxActivator ScopedContext(s_GlobalContext);
    // Do whatever work here
    // Destructor automatically deactivates the context
}

void MyInitializerFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};
    hActCtx = CreateActCtx(&actctx);
    s_GlobalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
    // The static destructor for s_GlobalContext destroys the
    // activation context on component unload.
}
```



 

 



