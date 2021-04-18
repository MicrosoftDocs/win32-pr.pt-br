---
description: Modo exclusivo do DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Modo exclusivo do DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105760709"
---
# <a name="directdraw-exclusive-mode"></a>Modo exclusivo do DirectDraw

> [!Note]  
> Este tópico aplica-se somente ao VMR-7. No VMR-9, você habilita o modo exclusivo fornecendo seu próprio apresentador de alocador de modo exclusivo. Isso é relativamente simples se você usar o método [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) . O exemplo de VMR9Allocator mostra como implementar um apresentador de alocador personalizado.

 

No modo exclusivo do DirectDraw, um aplicativo assume o controle exclusivo do hardware de gráficos. Isso é útil para aplicativos como jogos, ou talvez aplicativos de vídeo de tela inteira. Normalmente, o VMR cria os objetos do DirectDraw e define o nível de cooperação como normal. No entanto, para executar o VMR no modo exclusivo do DirectDraw, o próprio aplicativo deve criar o objeto do DirectDraw e a superfície primária e chamar **SetCooperativeLevel** para especificar o modo exclusivo.

O VMR tem um apresentador de alocador especial que permite que ele seja executado no modo exclusivo do DirectDraw. Para configurar o VMR para usar este alocador-Presenter:

1.  Crie o gráfico de filtro e adicione o VMR a ele usando o método [**IFilterGraph:: addfiltro**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Para obter um exemplo de código, consulte [modo sem janela do VMR](vmr-windowless-mode.md).
2.  Criar o alocador de modo exclusivo-apresentador:
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  Configure o novo alocador-apresentador:
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Conecte o novo alocador-apresentador ao VMR.
5.  Compile o restante do grafo de filtro de maneira usual.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos de operação do VMR](vmr-modes-of-operation.md)
</dt> </dl>

 

 



