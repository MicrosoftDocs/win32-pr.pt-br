---
description: Modo exclusivo do DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Modo exclusivo do DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09199e04a221299676c21fbc2876af4b8149943a743101d34893d5563ed42482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016175"
---
# <a name="directdraw-exclusive-mode"></a>Modo exclusivo do DirectDraw

> [!Note]  
> Este tópico se aplica somente à VMR-7. Na VMR-9, você habilita o modo exclusivo fornecendo seu próprio modo exclusivo allocator-presenter. Isso será relativamente simples se você usar o [**método IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) O exemplo VMR9Allocator mostra como implementar um alocador-presenter personalizado.

 

No Modo Exclusivo do DirectDraw, um aplicativo assume controle exclusivo do hardware gráfico. Isso é útil para aplicativos como jogos ou, talvez, aplicativos de vídeo de tela inteira. Normalmente, a VMR cria os objetos DirectDraw e define o nível cooperativo como normal. No entanto, para executar a VMR no Modo Exclusivo do DirectDraw, o próprio aplicativo deve criar o objeto DirectDraw e a superfície primária e chamar **SetCooperativeLevel** para especificar o modo exclusivo.

A VMR tem um allocator-presenter especial que permite que ele seja executado no Modo Exclusivo do DirectDraw. Para configurar a VMR para usar este allocator-presenter:

1.  Crie o filtro Graph e adicione a VMR a ele usando o [**método IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) Para ver um exemplo de código, consulte [Modo sem janela da VMR.](vmr-windowless-mode.md)
2.  Crie o allocator-presenter do Modo Exclusivo:
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

    

3.  Configure o novo allocator-presenter:
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Conecte o novo allocator-presenter à VMR.
5.  Crie o restante do grafo de filtro das maneiras comuns.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos de operação de VMR](vmr-modes-of-operation.md)
</dt> </dl>

 

 



