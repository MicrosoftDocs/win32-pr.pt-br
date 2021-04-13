---
title: Criar os objetos de animação principais
description: Para usar a animação do Windows em seu aplicativo, a primeira etapa é criar um pequeno conjunto de objetos de animação principais.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- objetos do Gerenciador de animação animação do Windows, criando
- animação de objetos de temporizador de animação do Windows, criando
- Animação de objetos de biblioteca de transição do Windows, criando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd1cab32e72bf1382469ada52abeecee47b6a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366484"
---
# <a name="create-the-main-animation-objects"></a>Criar os objetos de animação principais

Para usar a animação do Windows em seu aplicativo, a primeira etapa é criar um pequeno conjunto de objetos de animação principais.

## <a name="overview"></a>Visão geral

Use a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar os objetos Gerenciador de animação, temporizador de animação e biblioteca de transição.

Esses objetos serão necessários para criar e exibir animações, de modo que normalmente não devem ser liberados até que o aplicativo seja desligado. Se não houver nenhuma chance de que qualquer retorno de chamada registrado possa ter criado um ciclo de referência, liberar os objetos será suficiente para uma limpeza adequada. Caso contrário, o aplicativo pode ser limpo limpando os retornos de chamada (passando **nulo** no lugar de cada) ou chamando o método de [**desligamento**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) do Gerenciador de animação.

## <a name="example-code"></a>Código de exemplo

O código de exemplo a seguir é extraído de MainWindow. cpp nos exemplos de animação do Windows; consulte o método CMainWindow:: InitializeAnimation.


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



Observe as seguintes definições de MainWindow. h.


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

Depois de concluir esta etapa, a próxima etapa é: [criar variáveis de animação](create-animation-variables.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationTimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Visão geral da animação do Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 