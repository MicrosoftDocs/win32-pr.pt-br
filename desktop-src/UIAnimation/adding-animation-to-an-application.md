---
title: Criar os objetos de animação principais
description: Para usar Windows animação em seu aplicativo, a primeira etapa é criar um pequeno conjunto de objetos de animação principais.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- objetos do gerenciador de animação Windows Animação , criando
- animação de objetos de temporizador Windows Animação , criando
- objetos de biblioteca de transição Windows Animação , criando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3023e5934581850bb6aa21e7d41d92642bb01fadfcf7531fcacabca74b411f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137399"
---
# <a name="create-the-main-animation-objects"></a>Criar os objetos de animação principais

Para usar Windows animação em seu aplicativo, a primeira etapa é criar um pequeno conjunto de objetos de animação principais.

## <a name="overview"></a>Visão geral

Use a [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o gerenciador de animação, o temporizador de animação e os objetos da biblioteca de transição.

Esses objetos serão necessários para criar e exibir animações, portanto, eles geralmente não devem ser liberados até que o aplicativo seja desligado. Se não houver nenhuma chance de qualquer retorno de chamada registrado ter criado um ciclo de referência, liberar os objetos é suficiente para uma limpeza adequada. Caso contrário, o aplicativo poderá limpar limpando os retornos de chamada (passando **NULL** no lugar de cada um) ou chamando o método Shutdown do gerenciador [**de**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) animação.

## <a name="example-code"></a>Código de exemplo

O código de exemplo a seguir é retirado de MainWindow.cpp nos exemplos Windows Animation; consulte o método CMainWindow::InitializeAnimation.


```C++
// Create the animation manager object

HRESULT hr = CoCreateInstance(
    CLSID_UIAnimationManager,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&m_pAnimationManager)
    );

if (SUCCEEDED(hr))
{
    // Create the animation timer object

    hr = CoCreateInstance(
        CLSID_UIAnimationTimer,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pAnimationTimer)
        );

    if (SUCCEEDED(hr))
    {
        // Create the transition library object

        hr = CoCreateInstance(
            CLSID_UIAnimationTransitionLibrary,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_PPV_ARGS(&m_pTransitionLibrary)
            );

        ...

    }

    ...

}
```



Observe as seguintes definições de MainWindow.h.


```
class CMainWindow
{

    ...

private:

    // Animation components

    IUIAnimationManager *m_pAnimationManager;
    IUIAnimationTimer *m_pAnimationTimer;
    IUIAnimationTransitionLibrary *m_pTransitionLibrary;

    ...

};
```



## <a name="next-step"></a>Próxima etapa

Depois de concluir esta etapa, a próxima etapa é: Criar [Variáveis de Animação](create-animation-variables.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Cocreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationTimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Windows Visão geral da animação](scenic-animation-api-overview.md)
</dt> </dl>

 

 