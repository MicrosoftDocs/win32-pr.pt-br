---
title: Visão geral da camada de depuração Direct2D
description: Visão geral da camada de depuração Direct2D
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833174e0d18b11e2384d838930d5508601cfceaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099984"
---
# <a name="direct2d-debug-layer-overview"></a><span data-ttu-id="db3e0-103">Visão geral da camada de depuração Direct2D</span><span class="sxs-lookup"><span data-stu-id="db3e0-103">Direct2D Debug Layer Overview</span></span>

<span data-ttu-id="db3e0-104">A camada de depuração Direct2D fornece mensagens de depuração de tempo de design para você minimizar a falha do aplicativo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="db3e0-104">The Direct2D debug layer provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="db3e0-105">Esta visão geral descreve os conceitos básicos da camada de depuração Direct2D.</span><span class="sxs-lookup"><span data-stu-id="db3e0-105">This overview describes the basics of the Direct2D debug layer.</span></span> <span data-ttu-id="db3e0-106">Ele pressupõe que você esteja familiarizado com a criação de aplicativos Direct2D básicos.</span><span class="sxs-lookup"><span data-stu-id="db3e0-106">It assumes that you are familiar with creating basic Direct2D applications.</span></span>

<span data-ttu-id="db3e0-107">Esta visão geral contém as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="db3e0-107">This overview contains the following sections.</span></span>

-   [<span data-ttu-id="db3e0-108">O que é a camada de depuração Direct2D</span><span class="sxs-lookup"><span data-stu-id="db3e0-108">What Is the Direct2D Debug Layer</span></span>](#what-is-the-direct2d-debug-layer)
-   [<span data-ttu-id="db3e0-109">Instalando a camada de depuração Direct2D</span><span class="sxs-lookup"><span data-stu-id="db3e0-109">Installing the Direct2D Debug Layer</span></span>](#installing-the-direct2d-debug-layer)
-   [<span data-ttu-id="db3e0-110">Habilitando a camada de depuração</span><span class="sxs-lookup"><span data-stu-id="db3e0-110">Enabling the Debug Layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="db3e0-111">Níveis de depuração</span><span class="sxs-lookup"><span data-stu-id="db3e0-111">Debug Levels</span></span>](#debug-levels)
-   [<span data-ttu-id="db3e0-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db3e0-112">Related topics</span></span>](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a><span data-ttu-id="db3e0-113">O que é a camada de depuração Direct2D</span><span class="sxs-lookup"><span data-stu-id="db3e0-113">What Is the Direct2D Debug Layer</span></span>

<span data-ttu-id="db3e0-114">A camada de depuração Direct2D, implementada separadamente de Direct2D em sua própria DLL chamada d2d1debug.dll, fornece mensagens de depuração para permitir que você use com precisão as funções do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="db3e0-114">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides debug messages to enable you to accurately use Direct2D functions.</span></span> <span data-ttu-id="db3e0-115">As mensagens de depuração geralmente resultam de violações de contrato de API, como parâmetros inválidos (podem ser relacionados a Direct3D), recursos inválidos, violações de threading e problemas de desempenho, como usar uma camada quando um clipe seria suficiente.</span><span class="sxs-lookup"><span data-stu-id="db3e0-115">The debug messages often result from API contract violations such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and performance issues such as using a layer when a clip would suffice.</span></span> <span data-ttu-id="db3e0-116">Para especificar a quantidade de informações rastreadas pela camada de depuração, você pode especificar um dos três níveis de depuração: informações, aviso e erro; e uma mensagem de erro de nível dispara o ponto de interrupção para ajudá-lo a depurar.</span><span class="sxs-lookup"><span data-stu-id="db3e0-116">To specify how much information is traced by the debug layer, you can specify one of the three debug levels: information, warning, and error; and a message of level error triggers the breakpoint to help you debug.</span></span>

## <a name="installing-the-direct2d-debug-layer"></a><span data-ttu-id="db3e0-117">Instalando a camada de depuração Direct2D</span><span class="sxs-lookup"><span data-stu-id="db3e0-117">Installing the Direct2D Debug Layer</span></span>

<span data-ttu-id="db3e0-118">Para obter instruções sobre como instalar a camada de depuração, consulte [instalando a camada de depuração Direct2D](installing-the-direct2d-debug-layer.md).</span><span class="sxs-lookup"><span data-stu-id="db3e0-118">For instructions on installing the debug layer, see [Installing the Direct2D Debug Layer](installing-the-direct2d-debug-layer.md).</span></span>

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="db3e0-119">Habilitando a camada de depuração</span><span class="sxs-lookup"><span data-stu-id="db3e0-119">Enabling the Debug Layer</span></span>

<span data-ttu-id="db3e0-120">Para habilitar a camada de depuração em seu aplicativo, especifique um valor de [**\_ \_ nível de depuração d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) diferente de **d2d1 \_ nível de depuração \_ \_ nenhum** ao criar uma fábrica com a função [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .</span><span class="sxs-lookup"><span data-stu-id="db3e0-120">To enable the debug layer in your application, specify a [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) value other than **D2D1\_DEBUG\_LEVEL\_NONE** when you create a factory with the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>

> [!Note]  
> <span data-ttu-id="db3e0-121">Se a camada de depuração Direct2D estiver habilitada, o efeito de gerenciamento de cores Direct2D (CLSID \_ D2D1ColorManagement) poderá causar uma violação de acesso ao definir um contexto de cor.</span><span class="sxs-lookup"><span data-stu-id="db3e0-121">If the Direct2D debug layer is enabled, the Direct2D color management effect (CLSID\_D2D1ColorManagement) may cause an access violation when setting a color context.</span></span> <span data-ttu-id="db3e0-122">A solução alternativa é desabilitar a camada de depuração ao usar o efeito de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="db3e0-122">The workaround is to disable the debug layer when using the color management effect</span></span>

 

<span data-ttu-id="db3e0-123">Habilitar a camada de depuração para uma fábrica também permite a depuração de informações para qualquer objeto criado por essa fábrica.</span><span class="sxs-lookup"><span data-stu-id="db3e0-123">Enabling the debug layer for a factory also enables debugging information for any object created by that factory.</span></span>

<span data-ttu-id="db3e0-124">O exemplo a seguir habilita a camada de depuração para uma fábrica quando o aplicativo é compilado para a configuração de compilação de depuração.</span><span class="sxs-lookup"><span data-stu-id="db3e0-124">The following example enables the debug layer for a factory when the application is compiled for the DEBUG build configuration.</span></span>


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> <span data-ttu-id="db3e0-125">Se nenhuma opção de fábrica for especificada ou um nível de depuração de "None" for especificado, a camada de depuração não será invocada.</span><span class="sxs-lookup"><span data-stu-id="db3e0-125">If no factory options are specified or a debug level of "none" is specified, the debug layer is not invoked.</span></span> <span data-ttu-id="db3e0-126">A camada de depuração nunca deve estar ativa na versão de lançamento de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db3e0-126">The debug layer should never be active in the release version of an application.</span></span>

 

<span data-ttu-id="db3e0-127">A próxima seção descreve os diferentes níveis de depuração definidos pela enumeração de [**\_ \_ nível de depuração d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) .</span><span class="sxs-lookup"><span data-stu-id="db3e0-127">The next section describes the different debug levels defined by the [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration.</span></span>

## <a name="debug-levels"></a><span data-ttu-id="db3e0-128">Níveis de depuração</span><span class="sxs-lookup"><span data-stu-id="db3e0-128">Debug Levels</span></span>

<span data-ttu-id="db3e0-129">A enumeração de [**\_ \_ nível de depuração d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) especifica três níveis de depuração: \_ \_ \_ erro de nível de depuração d2d1 (erro), \_ aviso de \_ nível de depuração d2d1 \_ (aviso) e \_ informações de \_ nível de depuração d2d1 \_ (informações).</span><span class="sxs-lookup"><span data-stu-id="db3e0-129">The [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration specifies three debug levels: D2D1\_DEBUG\_LEVEL\_ERROR (error), D2D1\_DEBUG\_LEVEL\_WARNING (warning), and D2D1\_DEBUG\_LEVEL\_INFORMATION (information).</span></span> <span data-ttu-id="db3e0-130">Esses níveis são interpretados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="db3e0-130">These levels are interpreted as follows:</span></span>

-   <span data-ttu-id="db3e0-131">**Erro:** Direct2D envia mensagens de erro graves para a camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="db3e0-131">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="db3e0-132">Por exemplo, interromper uma restrição de Threading irá gerar um erro grave.</span><span class="sxs-lookup"><span data-stu-id="db3e0-132">For example, breaking a threading constraint will generate a severe error.</span></span>

-   <span data-ttu-id="db3e0-133">**AVISO:** O Direct2D envia mensagens de erro e avisos para a camada de depuração para que você possa endereçar qualquer uma dessas mensagens.</span><span class="sxs-lookup"><span data-stu-id="db3e0-133">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="db3e0-134">**Informações:** O Direct2D envia mensagens de erro, avisos e informações adicionais de diagnóstico para a camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="db3e0-134">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="db3e0-135">Por exemplo, as mensagens de melhoria de desempenho serão enviadas neste nível de depuração.</span><span class="sxs-lookup"><span data-stu-id="db3e0-135">For example, performance improvement messages will be sent at this debug level.</span></span>

<span data-ttu-id="db3e0-136">O valor D2D1 \_ nível de depuração \_ \_ None (None) indica que o Direct2D não fornece nenhuma saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="db3e0-136">The value D2D1\_DEBUG\_LEVEL\_NONE (none) indicates that Direct2D does not provide any debugging output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db3e0-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db3e0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db3e0-138">Mensagens de depuração</span><span class="sxs-lookup"><span data-stu-id="db3e0-138">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




