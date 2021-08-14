---
description: Esta documentação refere-se especificamente às extensões Windows Vista para gráficos DirectX.
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Resumo do recurso (Direct3D 9 para Windows Vista)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242af80fa4d6f00c1e55d4852884f9fbbf8de287c6792b3b4aaaad196a6cd113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523073"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>Resumo do recurso (Direct3D 9 para Windows Vista)

Esta documentação refere-se especificamente às extensões Windows Vista para gráficos DirectX. Para desenvolver o poder do DirectX para Windows Vista, você deve instalar o SDK do Windows Vista, bem como o SDK do DirectX. Os aplicativos que usam o DirectX para Windows Vista devem estar usando hardware que usa o driver WDDM (Windows Device Driver Model) em vez do XPDM (Modelo de Driver XP); drivers que não implementam o WDDM não podem insinciar Windows interfaces gráficas do Vista DirectX.

Descubra os novos recursos gráficos do DirectX Windows Vista em uma destas seções:

-   [Alterações de comportamento do dispositivo](#device-behavior-changes)
-   [Desabilitando o processamento de vértice de software multithread](#disabling-multithreaded-software-vertex-processing)
-   [Superfícies de um bit](#one-bit-surfaces)
-   [Profundidade de leitura/buffers de estêncil](#reading-depthstencil-buffers)
-   [Compartilhamento de recursos](#sharing-resources)
-   [Conversão de sRGB antes do blending](#srgb-conversion-before-blending)
-   [Melhorias do StretchRect](#stretchrect-improvements)
-   [Criação de textura na memória do sistema](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>Alterações de comportamento do dispositivo

Os dispositivos agora só são perdidos em duas circunstâncias; quando o hardware é redefinido porque está suspenso e quando o driver de dispositivo é interrompido. Quando o hardware trava, o dispositivo pode ser redefinido chamando [**ResetEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex) Se o hardware for travado, a memória da textura será perdida.

Depois que um driver é interrompido, o objeto IDirect9Ex deve ser recriado para retomar a renderização.

Quando a área de apresentação for obscurecida por outra janela no modo de janela ou quando um aplicativo de tela inteira for minimizado, [**o PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) retornará S \_ D3DPRESENTATIONOCCLUDED. Os aplicativos de tela inteira podem retomar a renderização quando recebem uma mensagem de retorno de chamada [**WM \_ ACTIVATEAPP.**](../winmsg/wm-activateapp.md)

Nas versões anteriores do DirectX, quando um aplicativo passou por uma alteração de modo, a única maneira de recuperar era redefinir o dispositivo e criar novamente todos os recursos de memória de vídeo e trocar cadeias. Agora com o DirectX para Windows Vista, chamar Redefinir após uma alteração de modo não faz com que superfícies de memória de textura, texturas e informações de estado sejam perdidas e esses recursos não precisam ser recriados.

## <a name="disabling-multithreaded-software-vertex-processing"></a>Desabilitando o processamento de vértice de software multithread

Um novo bit caps (D3DCREATE DISABLE PSGP THREADING) foi adicionado que desabilitará o multithreading para processamento de vértice \_ \_ de software \_ (swvp). Use essa macro para gerar um sinalizador de comportamento para IDirect3D9::CreateDevice.


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>Superfícies de um bit

Há um novo tipo de formato de superfície de um bit que pode ser especialmente útil para processar glifos de texto. O novo formato é chamado D3DFMT \_ A1. Uma superfície de um bit foi projetada para ser usada como uma textura por pixel ou a saída de destino de renderização gerada por ComposeRects ou ColorFill. Não há limites separados para a largura e a altura da superfície; uma implementação deve dar suporte a uma superfície de tamanho único de 2K x 8K texels.

Uma superfície de um bit tem um bit por texel; portanto, um significa que todos os componentes (r, g, b,a) de um pixel são 1 e zero significa que todos os componentes são iguais a 0. Você pode usar superfícies de um bit com as seguintes APIs: ColorFill, UpdateSurface e UpdateTexture.

Quando uma superfície de um bit é lida, o runtime pode executar a filtragem de amostra de ponto ou convolução. O filtro de convolução é ajustável (consulte [**SetConvolutionMonoKernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)).

Há algumas restrições para superfícies de um bit:

-   Não há suporte para mapeamento de Mip
-   Os dados sRGB não podem ser lidos ou gravados em uma superfície de um bit.
-   Uma superfície de um bit não pode ser usada como uma textura de vértice ou para multisampling.

## <a name="reading-depthstencil-buffers"></a>Profundidade de leitura/buffers de estêncil

Use IDirect3DDevice9::UpdateSurface para ler ou gravar dados de profundidade/estêncil de superfícies obtidas de IDirect3DDevice9::CreateDepthStencilSurface ou IDirect3DDevice9::GetDepthStencilSurface.

Primeiro, crie uma superfície somente de estêncil, de profundidade ou de bloqueio usando IDirect3DDevice9::CreateOffscreenPlainSurface. Use um destes formatos:

-   D3DFMT \_ D16 \_ LOCKABLE
-   D3DFMT \_ D32F \_ LOCKABLE
-   D3DFMT \_ D32 \_ LOCKABLE
-   D3DFMT \_ S8 \_ LOCKABLE

Em segundo lugar, transfira dados entre o buffer de profundidade/estêncil e a superfície de estêncil ou profundidade de bloqueio recém-criada. A transferência é executada usando IDirect3DDevice9::UpdateSurface.

UpdateSurface falhará quando ambas as superfícies são um formato LOCKABLE ou ambas não são bloqueáveis.

A transferência de dados inexistentes resultará em um erro (por exemplo, a transferência de uma superfície somente de profundidade não bloqueável para uma superfície LOCKABLE de D3DFMT \_ \_ S8).

O restante das restrições para IDirect3DDevice9::UpdateSurface ainda se aplica.

## <a name="sharing-resources"></a>Compartilhamento de recursos

Os recursos do Direct3D agora podem ser compartilhados entre dispositivos ou processos. Isso se aplica a qualquer recurso direct3D, incluindo texturas, buffers de vértice, buffers de índice ou superfícies (como destinos de renderização, buffers de estêncil de profundidade ou superfícies simples fora da tela). Para ser compartilhado, você precisa designar um recurso para compartilhamento no momento da criação e localizar o recurso no pool padrão (D3DPOOL \_ DEFAULT). Depois que um recurso é criado para compartilhamento, ele pode ser compartilhado entre dispositivos dentro de um processo ou compartilhado entre processos.

Para habilitar recursos compartilhados, as APIs de criação de recursos têm um parâmetro de alça adicional. Esse é um HANDLE que aponta para o recurso compartilhado. Nas revisões anteriores do DirectX, esse argumento fazia parte da assinatura da API, mas não foi usada e deve ser definido como **NULL.** Começando com Windows Vista, use pSharedHandle das seguintes maneiras:

-   De definir o ponteiro (pSharedHandle) como **NULL** para não compartilhar um recurso. Isso é exatamente como o comportamento do DirectX antes do Windows Vista.
-   Para criar um recurso compartilhado, chame qualquer API de criação de recursos (veja abaixo) com um alça não reinicializado (o ponteiro em si não é **NULL** (pSharedHandle != **NULL),** mas o ponteiro aponta para um valor **NULL** ( \* pSharedHandle == **NULL**)). A API gerará um recurso compartilhado e retornará um handle válido.
-   Para abrir e acessar um recurso compartilhado criado anteriormente usando um alça de recurso compartilhado nãoNULL, de definido pSharedHandle como o endereço desse handle. Depois de abrir o recurso compartilhado criado anteriormente dessa maneira, você pode usar a interface retornada na API direct3D 9 ou Direct3D 9Ex como se a interface fosse um recurso típico desse tipo.

As APIs de criação de recursos incluem [**- CreateTexture**](/windows/desktop/api), [**CreateVolumeTexture**](/windows/desktop/api), [**CreateCubeTexture**](/windows/desktop/api), [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget), [**CreateVertexBuffer**](/windows/desktop/api), [**CreateIndexBuffer**](/windows/desktop/api), [**CreateDepthStencilSurface**](/windows/desktop/api), [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateDepthStencilSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex), [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)e [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex).

Há algumas restrições para usar recursos compartilhados. Elas incluem:

-   A API usada para abrir um recurso compartilhado deve corresponder à API usada para criar o recurso compartilhado. Por exemplo, se você usou [**CreateTexture**](/windows/desktop/api) para criar um recurso compartilhado, deverá usar **CreateTexture** para abrir esse recurso compartilhado; Se você usou [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) para criar um recurso compartilhado, deverá usar **CreateRenderTarget** para abrir esse recurso compartilhado e assim por diante.
-   Ao abrir um recurso compartilhado, você deve especificar D3DPOOL \_ DEFAULT.
-   Recursos bloqueáveis (texturas com D3DUSAGE DYNAMIC, buffers de vértice e buffers de índice, por exemplo) podem ter um desempenho \_ ruim quando compartilhados. Os rendertargets que podem ser bloqueios não serão compartilhados em algum hardware.
-   As referências a um recurso compartilhado entre processos devem ter as mesmas dimensões que o recurso original. Ao passar um handle pelo processo, inclua as informações de dimensão para que a referência possa ser criada de forma idêntica.
-   Superfícies entre processos compartilhados não fornecem nenhum mecanismo de sincronização. Alterações de leitura/gravação em uma superfície compartilhada podem não refletir a exibição de um processo de referência da superfície quando esperado. Para fornecer sincronização, use consultas de evento ou bloqueie a textura.
-   Somente o processo que cria inicialmente um recurso compartilhado pode bloqueá-lo (qualquer processo que abra uma referência a esse recurso compartilhado não pode bloqueá-lo).
-   Se um recurso compartilhado estiver bloqueado, não haverá nenhuma validação para outros processos saberem se o recurso está disponível.

## <a name="srgb-conversion-before-blending"></a>Conversão de sRGB antes do blending

Agora você pode verificar se o dispositivo pode converter dados de pipeline em sRGB antes da combinação de buffer de quadro. Isso implica que o dispositivo converte os valores de destino de renderização de sRGB. Para ver se a conversão é suportada pelo hardware, verifique este limite:


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



Esse limite identifica o hardware que dá suporte à conversão para sRGB antes da mesclagem. Essa funcionalidade é importante para a renderização de alta qualidade de buffers de quadros fp16 no DWM (gerenciador de janelas da área de trabalho).

## <a name="stretchrect-improvements"></a>Melhorias do StretchRect

Nas versões anteriores do DirectX, o StretchRect tem muitas restrições para acomodar drivers diferentes (consulte IDirect3DDevice9::StretchRect). Windows O Vista é criado com base Windows WDDM (Modelo de Driver de Dispositivo). Esse novo modelo de driver é muito mais robusto e permite que os drivers lidam com casos especiais no hardware.

Em geral, a única restrição restante é que o destino de renderização deve ter sido criado com uso de destino de renderização (D3DUSAGE \_ RENDERTARGET). Essa restrição será retirada se você estiver fazendo uma cópia simples (em que a origem e o dest são do mesmo formato, mesmo tamanho e não há sub retângulos).

## <a name="texture-creation-in-system-memory"></a>Criação de textura na memória do sistema

Os aplicativos que precisam de mais flexibilidade sobre o uso, a alocação e a exclusão da memória do sistema agora podem criar texturas de um ponteiro de memória do sistema. Por exemplo, um aplicativo pode criar uma textura Direct3D de um ponteiro de bitmap de memória do sistema GDI.

Você precisa fazer duas coisas para criar essa textura:

-   Alocar memória suficiente do sistema para manter a superfície de textura. O número mínimo de bytes é largura x altura x bytes por pixel.
-   Passe o endereço de um ponteiro para a superfície de memória do sistema para o parâmetro HANDLE \* para IDirect3DDevice9::CreateTexture.

Aqui está o protótipo de função para IDirect3DDevice9::CreateTexture:


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



Uma textura de memória do sistema tem as seguintes restrições:

-   O tom de textura deve ser igual à largura da textura vezes o número de bytes por pixel.
-   Ao usar formatos compactados (formatos DXT), o aplicativo é responsável por alocar o tamanho correto.
-   Há suporte apenas para texturas com um único nível de mipmap.
-   O valor passado para CreateTexture para o argumento Pool deve ser D3DPOOL \_ SYSTEMMEM.
-   Essa API envolve a memória fornecida em uma textura. Não desalocar essa memória até que você faça isso.

 

 
