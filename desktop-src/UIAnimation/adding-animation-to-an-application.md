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
# <a name="create-the-main-animation-objects"></a><span data-ttu-id="ed28f-106">Criar os objetos de animação principais</span><span class="sxs-lookup"><span data-stu-id="ed28f-106">Create the Main Animation Objects</span></span>

<span data-ttu-id="ed28f-107">Para usar a animação do Windows em seu aplicativo, a primeira etapa é criar um pequeno conjunto de objetos de animação principais.</span><span class="sxs-lookup"><span data-stu-id="ed28f-107">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span>

## <a name="overview"></a><span data-ttu-id="ed28f-108">Visão geral</span><span class="sxs-lookup"><span data-stu-id="ed28f-108">Overview</span></span>

<span data-ttu-id="ed28f-109">Use a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar os objetos Gerenciador de animação, temporizador de animação e biblioteca de transição.</span><span class="sxs-lookup"><span data-stu-id="ed28f-109">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create the animation manager, animation timer, and transition library objects.</span></span>

<span data-ttu-id="ed28f-110">Esses objetos serão necessários para criar e exibir animações, de modo que normalmente não devem ser liberados até que o aplicativo seja desligado.</span><span class="sxs-lookup"><span data-stu-id="ed28f-110">These objects will be needed to create and display animations, so they usually should not be released until the application is shutting down.</span></span> <span data-ttu-id="ed28f-111">Se não houver nenhuma chance de que qualquer retorno de chamada registrado possa ter criado um ciclo de referência, liberar os objetos será suficiente para uma limpeza adequada.</span><span class="sxs-lookup"><span data-stu-id="ed28f-111">If there is no chance that any registered callbacks could have created a reference cycle, releasing the objects is sufficient for a proper cleanup.</span></span> <span data-ttu-id="ed28f-112">Caso contrário, o aplicativo pode ser limpo limpando os retornos de chamada (passando **nulo** no lugar de cada) ou chamando o método de [**desligamento**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) do Gerenciador de animação.</span><span class="sxs-lookup"><span data-stu-id="ed28f-112">Otherwise, the application can clean up by clearing the callbacks (passing **NULL** in the place of each) or by calling the animation manager's [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method.</span></span>

## <a name="example-code"></a><span data-ttu-id="ed28f-113">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="ed28f-113">Example Code</span></span>

<span data-ttu-id="ed28f-114">O código de exemplo a seguir é extraído de MainWindow. cpp nos exemplos de animação do Windows; consulte o método CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="ed28f-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples; see the CMainWindow::InitializeAnimation method.</span></span>


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



<span data-ttu-id="ed28f-115">Observe as seguintes definições de MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="ed28f-115">Note the following definitions from MainWindow.h.</span></span>


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



## <a name="next-step"></a><span data-ttu-id="ed28f-116">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="ed28f-116">Next Step</span></span>

<span data-ttu-id="ed28f-117">Depois de concluir esta etapa, a próxima etapa é: [criar variáveis de animação](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="ed28f-117">After completing this step, the next step is: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed28f-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed28f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed28f-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="ed28f-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="ed28f-120">**IUIAnimationManager**</span><span class="sxs-lookup"><span data-stu-id="ed28f-120">**IUIAnimationManager**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[<span data-ttu-id="ed28f-121">**IUIAnimationTimer**</span><span class="sxs-lookup"><span data-stu-id="ed28f-121">**IUIAnimationTimer**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[<span data-ttu-id="ed28f-122">**IUIAnimationTransitionLibrary**</span><span class="sxs-lookup"><span data-stu-id="ed28f-122">**IUIAnimationTransitionLibrary**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[<span data-ttu-id="ed28f-123">Visão geral da animação do Windows</span><span class="sxs-lookup"><span data-stu-id="ed28f-123">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 