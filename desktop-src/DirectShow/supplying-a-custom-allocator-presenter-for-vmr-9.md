---
description: Fornecendo um Allocator-Presenter personalizado para VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Fornecendo um Allocator-Presenter personalizado para VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e5f87aaecf0b2e8576b60a2d0f6a8c74e60fcf0759a123015ded9136c079bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951715"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Fornecendo um Allocator-Presenter personalizado para VMR-9

Para usar um alocador-presenter personalizado com o filtro VMR-9 (Video Mixing Renderer 9), execute as seguintes etapas:

1.  Implemente uma classe que dá suporte às interfaces [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) e [**IVMRImagePresenter9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
2.  Chame **QueryInterface** no filtro VMR-9 para a interface [**IVMRFilterConfig9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9)
3.  Chame o [**método IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) e passe o sinalizador **sem \_ renderização VMR9Mode.**
4.  **QueryInterface** no filtro VMR-9 para a interface [**IVMRSurfaceAllocatorNotify9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9)
5.  Chame o [**método IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) e passe um ponteiro para o método [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) do alocador-presenter.
6.  Chame o método [**IVMRSurfaceAllocator9::AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) do alocador e passe um ponteiro para a interface IVMR-9 do filtro [**VMR-9AllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) do filtro VMR.
7.  Em sua implementação de [**IVMRSurfaceAllocator9::AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify), chame [**IVMRSurfaceAllocatorNotify9::SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) Passe um ponteiro para o dispositivo Direct3D e um indicador para o monitor em que o vídeo será exibido.
8.  Em sua implementação do método [**IVMRSurfaceAllocator9::InitializeDevice,**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) crie superfícies Direct3D que corresponderem aos parâmetros determinados no **método InitializeDevice.** Opcionalmente, você pode usar o método IVMR-9 do filtro [**VMR-9AllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) para alocar essas superfícies. Armazene os ponteiros de superfície em uma matriz.
    > [!Note]  
    > Se você quiser que a VMR-9 desenhe os quadros de vídeo em uma superfície de textura, adicione o sinalizador **\_ TextureSurface VMR9AllocFlag** à estrutura [**VMR9AllocationInfo.**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) Se o dispositivo não dá suporte a texturas no formato de vídeo nativo, talvez seja necessário criar uma superfície de textura separada e copiar os quadros de vídeo da superfície de vídeo para a textura.

     

9.  Durante o streaming, a VMR-9 obtém superfícies do allocator-presenter chamando o [**método IVMRSurfaceAllocator9::GetSurface.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) A VMR-9 especifica a superfície por seu índice dentro da matriz de superfície (etapa 8).
10. Apresente a imagem quando a VMR-9 chamar o [**método IVMRImagePresenter9::P resentImage.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) Os parâmetros incluem um ponteiro para a superfície direct3D que contém a imagem de vídeo.
11. Se o dispositivo Direct3D for perdido a qualquer momento, o alocador-presenter deverá restaurar o dispositivo e recriar as superfícies. Por exemplo, o dispositivo poderá ser perdido se o modo de exibição mudar ou o usuário mover a janela para outro monitor. Se o dispositivo Direct3D mudar, chame o método IVMR-9 do filtro [**IVMRSurfaceAllocatorNotify9::ChangeD3DDevice.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice)
12. Quando o streaming é interrompido, a VMR-9 chama o [**método IVMRSurfaceAllocator9::TerminateDevice.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) O allocator-presenter deve liberar todos os seus recursos do Direct3D.

Há algumas diferenças entre a VMR-7 e a VMR-9 na maneira como os alocadores-presenters personalizados são gerenciados:

-   O método [**AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) do filtro VMR-9 está disponível para o allocator-presenter usar ao alocar superfícies. Esse método torna desnecessário que um alocador-presenter personalizado encaminhe todas as chamadas para o alocador-presenter padrão. Por esse motivo, a CLSID do alocador-presenter padrão do filtro VMR-9 não é publicada.
-   Ao contrário da VMR-7, a VMR-9 não fornece um alocador-presenter especial do Modo Exclusivo do DirectDraw. O [**método IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) torna esse objeto desnecessário.
-   Para vídeo entrelaçado, a VMR-9 sempre desentrada o vídeo antes de apresentar a imagem. O allocator-presenter não é mais responsável por desalocar a imagem antes de exibi-la.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modo de reprodução sem renderização de VMR (alocador-presenters personalizados)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



