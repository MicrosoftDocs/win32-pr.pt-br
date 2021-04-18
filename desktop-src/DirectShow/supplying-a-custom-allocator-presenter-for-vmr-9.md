---
description: Fornecendo um Allocator-Presenter personalizado para o VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Fornecendo um Allocator-Presenter personalizado para o VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f004e119fc1cbfc167c2130852a4f59700706fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810213"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Fornecendo um Allocator-Presenter personalizado para o VMR-9

Para usar um apresentador de alocador personalizado com o filtro do processador de mixagem de vídeo 9 (VMR-9), execute as seguintes etapas:

1.  Implemente uma classe que dê suporte às interfaces [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) e [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9) .
2.  Chame **QueryInterface** no filtro do VMR-9 para a interface [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .
3.  Chame o método [**IVMRFilterConfig9:: Setrenderizamode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) e passe o sinalizador **de \_ renderização VMR9Mode** .
4.  **QueryInterface** no filtro do VMR-9 para a interface [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) .
5.  Chame o método [**IVMRSurfaceAllocatorNotify9:: AdviseSurfaceAllocator**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) e transmita um ponteiro para o método [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) de seu Presenter de alocador.
6.  Chame o método [**IVMRSurfaceAllocator9:: AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) do apresentador do seu alocador e passe um ponteiro para a interface [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) do filtro do VMR-9.
7.  Em sua implementação de [**IVMRSurfaceAllocator9:: AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify), Call [**IVMRSurfaceAllocatorNotify9:: SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) passe um ponteiro para o dispositivo Direct3D e um identificador para o monitor onde o vídeo será exibido.
8.  Em sua implementação do método [**IVMRSurfaceAllocator9:: InitializeDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) , Crie superfícies Direct3D que correspondam aos parâmetros fornecidos no método **InitializeDevice** . Opcionalmente, você pode usar o método [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) do filtro do VMR-9 para alocar essas superfícies. Armazene os ponteiros de superfície em uma matriz.
    > [!Note]  
    > Se você quiser que o VMR-9 desenhe os quadros de vídeo em uma superfície de textura, adicione o sinalizador **VMR9AllocFlag \_ TextureSurface** à estrutura [**VMR9AllocationInfo**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) . Se o dispositivo não oferecer suporte a texturas no formato de vídeo nativo, talvez seja necessário criar uma superfície de textura separada e, em seguida, copiar os quadros de vídeo da superfície de vídeo para a textura.

     

9.  Durante o streaming, o VMR-9 Obtém superfícies do apresentador de alocador chamando o método [**IVMRSurfaceAllocator9:: getsurface**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) . O VMR-9 especifica a superfície por seu índice dentro da matriz de superfície (etapa 8).
10. Apresente a imagem quando o VMR-9 chama o método [**IVMRImagePresenter9::P resentimage**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) . Os parâmetros incluem um ponteiro para a superfície do Direct3D que contém a imagem de vídeo.
11. Se o dispositivo Direct3D for perdido a qualquer momento, o apresentador de alocador deve restaurar o dispositivo e recriar as superfícies. Por exemplo, o dispositivo poderá ser perdido se o modo de exibição for alterado ou o usuário mover a janela para outro monitor. Se o dispositivo Direct3D for alterado, chame o método [**IVMRSurfaceAllocatorNotify9:: ChangeD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) do filtro do VMR-9.
12. Quando o streaming é interrompido, o VMR-9 chama o método [**IVMRSurfaceAllocator9:: TerminateDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) . O apresentador de alocador deve liberar todos os seus recursos do Direct3D.

Há algumas diferenças entre o VMR-7 e o VMR-9 no modo como os apresentadores personalizados de alocadores são gerenciados:

-   O método [**AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) do filtro do VMR-9 está disponível para o alocador de alocação a ser usado ao alocar superfícies. Esse método torna desnecessário que um apresentador de alocador personalizado encaminhe todas as chamadas ao apresentador de alocador padrão. Por esse motivo, o CLSID do padrão de alocador do filtro do VMR-9 não é publicado.
-   Ao contrário do VMR-7, o VMR-9 não fornece um apresentador de alocador de modo exclusivo do DirectDraw especial. O método [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) torna esse objeto desnecessário.
-   Para vídeo entrelaçado, o VMR-9 sempre desentrelaça o vídeo antes de apresentar a imagem. O alocador-Presenter não é mais responsável por desentrelaçar a imagem antes de exibi-la.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modo de reprodução do VMR (alocador personalizado-apresentadores)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



