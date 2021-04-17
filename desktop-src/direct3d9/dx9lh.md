---
description: Esta documentação refere-se especificamente às extensões do Windows Vista para elementos gráficos do DirectX.
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Resumo do recurso (Direct3D 9 para Windows Vista)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cf2447297b7f24edf7d0200e640d5aef90bff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105790508"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>Resumo do recurso (Direct3D 9 para Windows Vista)

Esta documentação refere-se especificamente às extensões do Windows Vista para elementos gráficos do DirectX. Para desenvolver o poder do DirectX para Windows Vista, você deve instalar o SDK do Windows Vista, bem como o SDK do DirectX. Os aplicativos que usam o DirectX para Windows Vista devem usar o hardware que usa o driver do WDDM (modelo de driver de dispositivo do Windows) em oposição ao XPDM (modelo de driver XP); os drivers que não implementam o WDDM não podem instanciar as interfaces gráficas do DirectX do Windows Vista.

Descubra os novos recursos gráficos do DirectX no Windows Vista em uma destas seções:

-   [Alterações de comportamento do dispositivo](#device-behavior-changes)
-   [Desabilitando o processamento de vértice de software multithread](#disabling-multithreaded-software-vertex-processing)
-   [Superfícies de um bit](#one-bit-surfaces)
-   [Lendo buffers de profundidade/estêncil](#reading-depthstencil-buffers)
-   [Compartilhando recursos](#sharing-resources)
-   [Conversão sRGB antes da mesclagem](#srgb-conversion-before-blending)
-   [Aprimoramentos do StretchRect](#stretchrect-improvements)
-   [Criação de textura na memória do sistema](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>Alterações de comportamento do dispositivo

Os dispositivos agora são perdidos apenas em duas circunstâncias; Quando o hardware é redefinido porque está suspenso e quando o driver do dispositivo é interrompido. Quando o hardware trava, o dispositivo pode ser redefinido chamando [**ResetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex). Se o hardware parar, a memória da textura será perdida.

Depois que um driver é interrompido, o objeto IDirect9Ex deve ser recriado para retomar a renderização.

Quando a área de apresentação é obscurecida por outra janela no modo de janela ou quando um aplicativo de tela inteira é minimizado, [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) retornará S \_ D3DPRESENTATIONOCCLUDED. Aplicativos de tela inteira podem retomar a renderização quando recebem uma mensagem de retorno de chamada do [**WM \_ ACTIVATEAPP**](../winmsg/wm-activateapp.md) .

Nas versões anteriores do DirectX, quando um aplicativo sofreu uma alteração no modo, a única maneira de recuperar era redefinir o dispositivo e recriar todos os recursos de memória de vídeo e trocar cadeias. Agora, com o DirectX para Windows Vista, chamar Reset após uma alteração de modo não faz com que as superfícies de memória de textura, texturas e informações de estado sejam perdidas e que esses recursos não precisem ser recriados.

## <a name="disabling-multithreaded-software-vertex-processing"></a>Desabilitando o processamento de vértice de software multithread

Um novo bit de Caps (D3DCREATE \_ Disable \_ PSGP \_ Threading) foi adicionado para desabilitar o multithreading para o swvp (processamento de vértices de software). Use esta macro para gerar um sinalizador de comportamento para IDirect3D9:: CreateDevice.


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>Superfícies de um bit

Há um novo tipo de formato de superfície de bit que pode ser especialmente útil para processar glifos de texto. O novo formato é chamado de D3DFMT \_ a1. Uma superfície de um bit é projetada para ser usada como uma textura por pixel ou a saída de destino de renderização gerada por ComposeRects ou ColorFill. Não há limites separados para a largura e a altura da superfície; uma implementação deve dar suporte a uma superfície de tamanho único que seja de 2K texels x 8K texels.

Uma superfície de um bit tem um bit por Texel; Portanto, uma delas significa que todos os componentes (r, g, b, a) de um pixel são 1 e zero significaria que todos os componentes são iguais a 0. Você pode usar superfícies de um bit com as seguintes APIs: ColorFill, UpdateSurface e UpdateTexture.

Quando uma superfície de um bit é lida, o tempo de execução pode executar a amostra de ponto ou a filtragem de convolução. O filtro de convolução é ajustável (consulte [**SetConvolutionMonoKernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)).

Há algumas restrições para superfícies de um bit:

-   Não há suporte para o mapeamento MIP
-   os dados sRGB não podem ser lidos ou gravados em uma superfície de um bit.
-   Uma superfície de um bit não pode ser usada como uma textura de vértice ou para multiamostragem.

## <a name="reading-depthstencil-buffers"></a>Lendo buffers de profundidade/estêncil

Use IDirect3DDevice9:: UpdateSurface para ler ou gravar dados de profundidade/estêncil de superfícies obtidas de IDirect3DDevice9:: CreateDepthStencilSurface ou IDirect3DDevice9:: GetDepthStencilSurface.

Primeiro, crie uma superfície de bloqueáveis, somente profundidade ou apenas de estêncil usando IDirect3DDevice9:: CreateOffscreenPlainSurface. Use um destes formatos:

-   D3DFMT \_ D16 \_ bloqueáveis
-   D3DFMT \_ D32F \_ bloqueáveis
-   D3DFMT \_ D32 \_ bloqueáveis
-   D3DFMT \_ S8 \_ bloqueáveis

Em segundo lugar, transfira dados entre o buffer de profundidade/estêncil e a profundidade de bloqueáveis ou a superfície de estêncil criada recentemente. A transferência é executada usando IDirect3DDevice9:: UpdateSurface.

UpdateSurface falhará quando as duas superfícies forem um formato BLOQUEÁVEIS ou se ambas não forem bloqueáveis.

A transferência de dados inexistentes resultará em um erro (por exemplo, transferindo de uma superfície não bloqueáveis somente profundidade para uma \_ superfície D3DFMT S8 \_ bloqueáveis).

O restante das restrições para IDirect3DDevice9:: UpdateSurface ainda se aplica.

## <a name="sharing-resources"></a>Compartilhando recursos

Os recursos do Direct3D agora podem ser compartilhados entre dispositivos ou processos. Isso se aplica a qualquer recurso do Direct3D, incluindo texturas, buffers de vértice, buffers de índice ou superfícies (como destinos de renderização, buffers de estêncil de profundidade ou superfícies simples fora da tela). Para ser compartilhado, você precisa designar um recurso para compartilhamento no momento da criação e localizar o recurso no pool padrão ( \_ padrão D3DPOOL). Depois que um recurso é criado para compartilhamento, ele pode ser compartilhado entre dispositivos dentro de um processo ou compartilhado entre processos.

Para habilitar recursos compartilhados, as APIs de criação de recursos têm um parâmetro de identificador adicional. Trata-se de um identificador que aponta para o recurso compartilhado. Nas revisões anteriores do DirectX, esse argumento faz parte da assinatura de API, mas não foi usado e deve ser definido como **NULL**. A partir do Windows Vista, use o pSharedHandle das seguintes maneiras:

-   Defina o ponteiro (pSharedHandle) como **nulo** para não compartilhar um recurso. Isso é exatamente como o comportamento do DirectX antes do Windows Vista.
-   Para criar um recurso compartilhado, chame qualquer API de criação de recurso (veja abaixo) com um identificador não inicializado (o próprio ponteiro não é **nulo** (pSharedHandle! = **NULL**), mas o ponteiro aponta para um valor **nulo** ( \* pSharedHandle = = **NULL**)). A API irá gerar um recurso compartilhado e retornar um identificador válido.
-   Para abrir e acessar um recurso compartilhado criado anteriormente usando um identificador de recurso compartilhado não nulo, defina pSharedHandle como o endereço desse identificador. Depois de abrir o recurso compartilhado criado anteriormente dessa maneira, você pode usar a interface retornada na API Direct3D 9 ou Direct3D 9Ex como se a interface fosse um recurso típico desse tipo.

As APIs de criação de recursos incluem- [**CreateTexture**](/windows/desktop/api), [**CreateVolumeTexture**](/windows/desktop/api), [**CreateCubeTexture**](/windows/desktop/api), [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget), [**CreateVertexBuffer**](/windows/desktop/api), [**CreateIndexBuffer**](/windows/desktop/api), [**CreateDepthStencilSurface**](/windows/desktop/api), [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateDepthStencilSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex), [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)e [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex).

Há algumas restrições para o uso de recursos compartilhados. Estão incluídos:

-   A API que você usa para abrir um recurso compartilhado deve corresponder à API que você usou para criar o recurso compartilhado. Por exemplo, se você usou [**CreateTexture**](/windows/desktop/api) para criar um recurso compartilhado, deverá usar **CreateTexture** para abrir esse recurso compartilhado; Se você usou o [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) para criar um recurso compartilhado, deverá usar o **CreateRenderTarget** para abrir esse recurso compartilhado e assim por diante.
-   Ao abrir um recurso compartilhado, você deve especificar D3DPOOL \_ padrão.
-   Os recursos de bloqueáveis (texturas com D3DUSAGE \_ dinâmico, buffers de vértice e buffers de índice, por exemplo) podem experimentar mau desempenho quando compartilhados. O bloqueáveis rendertargets não será compartilhado em alguns hardwares.
-   As referências a um recurso compartilhado entre processos devem ter as mesmas dimensões que o recurso original. Ao passar um identificador pelo processo, inclua as informações de dimensão para que a referência possa ser criada de forma idêntica.
-   As superfícies de processo cruzado compartilhado não fornecem nenhum mecanismo de sincronização. As alterações de leitura/gravação em uma superfície compartilhada podem não refletir a exibição de um processo de referência da superfície quando esperado. Para fornecer sincronização, use consultas de evento ou bloqueie a textura.
-   Somente o processo que inicialmente cria um recurso compartilhado pode bloqueá-lo (qualquer processo que abra uma referência a esse recurso compartilhado não pode bloqueá-lo).
-   Se um recurso compartilhado estiver bloqueado, não haverá validação para outros processos saber se o recurso está disponível.

## <a name="srgb-conversion-before-blending"></a>Conversão sRGB antes da mesclagem

Agora você pode verificar se o dispositivo pode converter dados de pipeline para sRGB antes da mistura de buffer de quadro. Isso implica que o dispositivo converte os valores de destino de renderização de sRGB. Para ver se a conversão é suportada pelo hardware, verifique este limite:


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



Esse limite identifica o hardware que dá suporte à conversão para sRGB antes da mesclagem. Esse recurso é importante para o processamento de alta qualidade de buffers de quadros FP16 no DWM (Gerenciador de janelas da área de trabalho).

## <a name="stretchrect-improvements"></a>Aprimoramentos do StretchRect

Nas versões anteriores do DirectX, o StretchRect tem muitas restrições para acomodar drivers diferentes (consulte IDirect3DDevice9:: StretchRect). O Windows Vista baseia-se no Windows Device Driver Model (WDDM). Esse novo modelo de driver é muito mais robusto e permite que os drivers manipulem casos especiais no hardware.

Em geral, a única restrição restante é que o destino de renderização deve ter sido criado com o uso de destino de renderização (D3DUSAGE \_ RENDERTARGET). Essa restrição será levantada se você estiver fazendo uma cópia simples (onde a origem e o destino têm o mesmo formato, o mesmo tamanho e não há subretângulos).

## <a name="texture-creation-in-system-memory"></a>Criação de textura na memória do sistema

Os aplicativos que precisam de mais flexibilidade sobre o uso, a alocação e a exclusão da memória do sistema agora podem criar texturas de um ponteiro de memória do sistema. Por exemplo, um aplicativo poderia criar uma textura de Direct3D a partir de um ponteiro de bitmap de memória do sistema GDI.

Você precisa fazer duas coisas para criar essa textura:

-   Aloque memória do sistema suficiente para manter a superfície de textura. O número mínimo de bytes é largura x altura x bytes por pixel.
-   Passe o endereço de um ponteiro para a superfície de memória do sistema para o \* parâmetro HANDLE para IDirect3DDevice9:: CreateTexture.

Este é o protótipo de função para IDirect3DDevice9:: CreateTexture:


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



Uma textura de memória do sistema tem as seguintes restrições:

-   A densidade da textura deve ser igual à largura da textura número de bytes por pixel.
-   Ao usar formatos compactados (formatos DXT), o aplicativo é responsável por alocar o tamanho correto.
-   Só há suporte para texturas com um único nível de mipmap.
-   O valor passado para CreateTexture para o argumento do pool deve ser D3DPOOL \_ SYSTEMMEM.
-   Essa API encapsula a memória fornecida em uma textura. Não desaloque esta memória até que você tenha feito isso.

 

 
