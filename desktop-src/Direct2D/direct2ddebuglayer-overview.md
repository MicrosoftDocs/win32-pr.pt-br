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
# <a name="direct2d-debug-layer-overview"></a>Visão geral da camada de depuração Direct2D

A camada de depuração Direct2D fornece mensagens de depuração de tempo de design para você minimizar a falha do aplicativo em tempo de execução. Esta visão geral descreve os conceitos básicos da camada de depuração Direct2D. Ele pressupõe que você esteja familiarizado com a criação de aplicativos Direct2D básicos.

Esta visão geral contém as seções a seguir.

-   [O que é a camada de depuração Direct2D](#what-is-the-direct2d-debug-layer)
-   [Instalando a camada de depuração Direct2D](#installing-the-direct2d-debug-layer)
-   [Habilitando a camada de depuração](#enabling-the-debug-layer)
-   [Níveis de depuração](#debug-levels)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a>O que é a camada de depuração Direct2D

A camada de depuração Direct2D, implementada separadamente de Direct2D em sua própria DLL chamada d2d1debug.dll, fornece mensagens de depuração para permitir que você use com precisão as funções do Direct2D. As mensagens de depuração geralmente resultam de violações de contrato de API, como parâmetros inválidos (podem ser relacionados a Direct3D), recursos inválidos, violações de threading e problemas de desempenho, como usar uma camada quando um clipe seria suficiente. Para especificar a quantidade de informações rastreadas pela camada de depuração, você pode especificar um dos três níveis de depuração: informações, aviso e erro; e uma mensagem de erro de nível dispara o ponto de interrupção para ajudá-lo a depurar.

## <a name="installing-the-direct2d-debug-layer"></a>Instalando a camada de depuração Direct2D

Para obter instruções sobre como instalar a camada de depuração, consulte [instalando a camada de depuração Direct2D](installing-the-direct2d-debug-layer.md).

## <a name="enabling-the-debug-layer"></a>Habilitando a camada de depuração

Para habilitar a camada de depuração em seu aplicativo, especifique um valor de [**\_ \_ nível de depuração d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) diferente de **d2d1 \_ nível de depuração \_ \_ nenhum** ao criar uma fábrica com a função [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .

> [!Note]  
> Se a camada de depuração Direct2D estiver habilitada, o efeito de gerenciamento de cores Direct2D (CLSID \_ D2D1ColorManagement) poderá causar uma violação de acesso ao definir um contexto de cor. A solução alternativa é desabilitar a camada de depuração ao usar o efeito de gerenciamento de cores

 

Habilitar a camada de depuração para uma fábrica também permite a depuração de informações para qualquer objeto criado por essa fábrica.

O exemplo a seguir habilita a camada de depuração para uma fábrica quando o aplicativo é compilado para a configuração de compilação de depuração.


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
> Se nenhuma opção de fábrica for especificada ou um nível de depuração de "None" for especificado, a camada de depuração não será invocada. A camada de depuração nunca deve estar ativa na versão de lançamento de um aplicativo.

 

A próxima seção descreve os diferentes níveis de depuração definidos pela enumeração de [**\_ \_ nível de depuração d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) .

## <a name="debug-levels"></a>Níveis de depuração

A enumeração de [**\_ \_ nível de depuração d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) especifica três níveis de depuração: \_ \_ \_ erro de nível de depuração d2d1 (erro), \_ aviso de \_ nível de depuração d2d1 \_ (aviso) e \_ informações de \_ nível de depuração d2d1 \_ (informações). Esses níveis são interpretados da seguinte maneira:

-   **Erro:** Direct2D envia mensagens de erro graves para a camada de depuração. Por exemplo, interromper uma restrição de Threading irá gerar um erro grave.

-   **AVISO:** O Direct2D envia mensagens de erro e avisos para a camada de depuração para que você possa endereçar qualquer uma dessas mensagens.

-   **Informações:** O Direct2D envia mensagens de erro, avisos e informações adicionais de diagnóstico para a camada de depuração. Por exemplo, as mensagens de melhoria de desempenho serão enviadas neste nível de depuração.

O valor D2D1 \_ nível de depuração \_ \_ None (None) indica que o Direct2D não fornece nenhuma saída de depuração.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mensagens de depuração](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




