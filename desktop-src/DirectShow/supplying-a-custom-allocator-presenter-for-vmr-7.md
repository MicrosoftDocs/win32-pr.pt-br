---
description: Fornecendo um Allocator-Presenter personalizado para o VMR-7
ms.assetid: 19b43c9b-2578-418f-b03b-af7c7a3a46e4
title: Fornecendo um Allocator-Presenter personalizado para o VMR-7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79f191401f990214b2551f9210fab4dfe4d43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559984"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-7"></a>Fornecendo um Allocator-Presenter personalizado para o VMR-7

O alocador-Presenter é responsável por alocar superfícies do DirectDraw e apresentar os quadros de vídeo para renderização. Na grande maioria dos cenários, a funcionalidade do apresentador de alocador padrão será mais do que suficiente para as necessidades de um aplicativo. Mas ao conectar um apresentador de alocador personalizado, um aplicativo pode obter acesso direto aos bits de vídeo e controlar completamente o processo de renderização. A desvantagem dessa maior potência é que o aplicativo deve lidar com a complexidade adicional do gerenciamento de superfície do DirectDraw.

![usando um apresentador de alocador personalizado](images/custom-ap.png)

A figura anterior mostra as interfaces de comunicação usadas pelo VMR e pelo alocador-Presenter. Um apresentador de alocador personalizado que substitui todas as funcionalidades padrão de alocação e apresentação deve implementar as interfaces [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) e [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) e, opcionalmente, [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol).

Para substituir o apresentador de alocador padrão, um aplicativo chama o método [**IVMRSurfaceAllocatorNotify:: AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) e passa um ponteiro para o novo apresentador de alocador. Em resposta a essa chamada, o VMR chamará o método [**IVMRSurfaceAllocator:: AdviseNotify**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocator-advisenotify) do apresentador-Presenter para fornecer o ponteiro para a interface [**IVMRSurfaceAllocatorNotify**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify) do VMR. O apresentador de alocador usará esse ponteiro de interface ao passar eventos para o VMR com o método [**IVMRSurfaceAllocatorNotify:: NotifyEvent**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-notifyevent) .

Como uma solução alternativa, um aplicativo pode usar seu próprio apresentador de alocador e o apresentador de alocador padrão. Nesse cenário, o apresentador de alocador personalizado trata apenas das chamadas em que a funcionalidade personalizada é necessária e passa o restante das chamadas do VMR até o alocador de origem padrão. Em muitos casos, só é necessário substituir a interface [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) .

![usando dois alocadores-apresentadores](images/custom-ap2.png)

Para usar um apresentador de alocador personalizado e o apresentador de alocador padrão, um aplicativo primeiro chamaria [**IVMRSurfaceAllocatorNotify:: AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) para fornecer um ponteiro para o novo apresentador de alocador. Isso faz com que o apresentador de alocador padrão seja destruído e, portanto, o aplicativo deve criar outra instância dele chamando **QueryInterface** no VMR e solicitando a interface [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) . Conforme mostrado na figura anterior, o apresentador de alocador personalizado substitui os métodos de interface [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) e simplesmente passa todas as chamadas para a interface **IVMRSurfaceAllocator** para a implementação padrão. A figura também mostra a interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) como sendo implementada no apresentador de alocador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fornecendo um Allocator-Presenter personalizado para o VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
</dt> <dt>

[Modo de reprodução do VMR (alocador personalizado-apresentadores)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



