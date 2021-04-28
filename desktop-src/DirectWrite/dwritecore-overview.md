---
title: Visão geral do DWriteCore
description: DWriteCore é a implementação de reunião do projeto de DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 4ab8970172032f47b6e97da6d097d7c1bf33e976
ms.sourcegitcommit: 133954d5dbcd5b2b3b50c8efd16cd101278fc1db
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108172498"
---
# <a name="dwritecore-overview"></a>Visão geral do DWriteCore

DWriteCore é a implementação de [reunião do projeto](/windows/apps/project-reunion/) de [DirectWrite](./direct-write-portal.md) (DirectWrite é a API do DirectX para renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução e suporte completo a texto Unicode e layout). O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.

Este tópico introdutório descreve o que é o DWriteCore e mostra como instalá-lo em seu ambiente de desenvolvimento e programar com ele.

## <a name="the-value-proposition-of-dwritecore"></a>A proposta de valor de DWriteCore

O [DirectWrite](./direct-write-portal.md) em si dá suporte a uma ampla gama de recursos que o torna a ferramenta de renderização de fontes de escolha no Windows para a maioria dos aplicativos &mdash; , seja por meio de chamadas diretas ou por meio de [Direct2D](../direct2d/direct2d-portal.md). O DirectWrite inclui um sistema de layout de texto independente de dispositivo, renderização de texto de alta qualidade de subpixel [do Microsoft ClearType](/typography/cleartype/) , texto acelerado por hardware, texto de vários formatos, recursos de tipografia de [® de OpenType](/typography/opentype/) avançados, suporte a todo o idioma e renderização e processamento compatíveis com [GDI](../gdi/windows-gdi.md). O DirectWrite está disponível desde o Windows Vista SP2 e evoluiu ao longo dos anos para incluir recursos mais avançados, como fontes variáveis, que permitem aplicar estilos, pesos e outros atributos a uma fonte com apenas um recurso de fonte.

No entanto, devido à longa vida útil do DirectWrite, os avanços no desenvolvimento têm o tendiam de deixar versões anteriores do Windows atrás. Além disso, o status do DirectWrite como a tecnologia de renderização de texto Premier é limitado apenas ao Windows, deixando aplicativos de plataforma cruzada para gravar sua própria pilha de renderização de texto ou para se basear em soluções de terceiros.

O DWriteCore resolve os problemas fundamentais de órfão de recursos de versão e compatibilidade entre plataformas removendo a biblioteca do sistema e direcionando todos os pontos de extremidade possíveis com suporte. Para esse fim, integramos o DWriteCore à reunião do projeto com uma API pública que tem suporte em todos os pontos de extremidade do Windows até o Windows 8 e abre a porta para que você o use entre plataformas.

O valor principal que o DWriteCore fornece a você, como desenvolvedor, na reunião do projeto, é que ele fornece acesso a todos os recursos atuais do DirectWrite, desde o nível inferior até o Windows 8. Todos os recursos do DWriteCore funcionarão da mesma forma em todas as versões de nível inferior; em outras palavras, todos os recursos atuais funcionarão no Windows 8, 8,1 e em todas as versões do Windows 10, sem qualquer diferença em relação a quais recursos podem funcionar em quais versões.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>O aplicativo de demonstração DWriteCore &mdash; DWriteCoreGallery

O DWriteCore é demonstrado por meio do aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , que está disponível para você agora para baixar e estudar.

## <a name="get-started-with-dwritecore"></a>Introdução ao DWriteCore

DWriteCore faz parte do [projeto reunião 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0). Esta seção descreve como configurar seu ambiente de desenvolvimento para a programação com o DWriteCore.

### <a name="install-the-project-reunion-05-vsix"></a>Instalar o VSIX do projeto reunião 0,5

No Visual Studio, clique em **extensões**  >  **gerenciar extensões**, pesquise por *reunião do projeto* e baixe a extensão de reunião do projeto. Feche e reabra o Visual Studio e siga os prompts para instalar a extensão.

Para obter mais informações, consulte [reunião do projeto 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)e [configurar seu ambiente de desenvolvimento (para a reunião do projeto)](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment).

### <a name="create-a-new-project"></a>Criar um novo projeto

No Visual Studio, crie um novo projeto do modelo de projeto **aplicativo em branco, empacotado (WinUI 3 no desktop)** . Você pode encontrar esse modelo de projeto escolhendo linguagem: *C++*; plataforma: *reunião do projeto*; tipo de projeto: *área de trabalho*.

Para obter mais informações, consulte Introdução [ao WinUI 3 para aplicativos da área de trabalho](/windows/apps/winui/winui3/get-started-winui3-for-desktop).

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>Instalar o pacote NuGet Microsoft. ProjectReunion. DWrite

No Visual Studio, clique em **projeto** \> **gerenciar pacotes NuGet...** \> **procure**, digite ou cole **Microsoft. ProjectReunion. DWrite** na caixa de pesquisa, selecione o item nos resultados da pesquisa e clique em **instalar** para instalar o pacote para esse projeto.

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>Como alternativa, comece com o aplicativo de exemplo DWriteCoreGallery

Como alternativa, você pode programar com DWriteCore começando com o projeto de aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) e basear seu desenvolvimento nesse projeto. Você pode, então, ficar à vontade para remover qualquer código-fonte (ou arquivos) existente desse projeto de exemplo e adicionar qualquer código-fonte (ou arquivos) novo ao projeto.

### <a name="use-dwritecore-in-your-project"></a>Usar o DWriteCore em seu projeto

Para obter mais informações sobre programação com o DWriteCore, consulte a seção [programação com DWriteCore](#programming-with-dwritecore) mais adiante neste tópico.

## <a name="the-release-phases-of-dwritecore"></a>As fases de lançamento do DWriteCore

Portar DirectWrite para DWriteCore é um projeto suficientemente grande para abranger vários ciclos de versão do Windows. Esse projeto é dividido em fases, cada uma correspondendo a uma parte da funcionalidade fornecida em uma versão.

### <a name="features-in-the-current-release-of-dwritecore"></a>Recursos na versão atual do DWriteCore

A versão do DWriteCore atualmente disponível faz parte do [projeto reunião 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0). Ele contém as ferramentas básicas que você, como desenvolvedor, precisam consumir o DWriteCore, incluindo os recursos a seguir.

- Enumeração de fontes.
- API de fonte.
- Dela.
- APIs de renderização de nível baixo. Isso é parcial na fase atual &mdash; DWriteCore não interopera com [Direct2D](../direct2d/direct2d-portal.md), mas você pode usar [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).
- Funcionalidade básica de layout de texto.
- APIs de renderização de texto.
- Destino de renderização de bitmap.
- Fontes de cores.
- Otimizações diversas (limpeza do cache de fontes, carregador de fonte em memória e assim por diante).

Um recurso de faixa é fontes de cores. As fontes de cores permitem que você processe suas fontes com funcionalidade de cores mais sofisticada além das simples cores únicas. Por exemplo, fontes de cor é o que capacita a capacidade de renderizar Emoji e fontes de ícone da barra de ferramentas (o último usado pelo Office, por exemplo). As fontes de cores foram introduzidas pela primeira vez no Windows 8.1, mas o recurso estava muito expandido no Windows 10, versão 1607 (atualização de aniversário).

O trabalho na limpeza do cache de fontes e no carregador de fontes na memória, permite o carregamento mais rápido de fontes e melhorias na memória.

Com esses recursos, você pode começar imediatamente a aproveitar algumas das principais funcionalidades do DirectWrite &mdash; , como fontes variáveis de &mdash; nível inferior para o Windows 8. Fontes de variáveis são um dos recursos mais importantes para clientes do DirectWrite; Eles foram introduzidos no Windows 10, versão 1709 (atualização para criadores de outono), portanto, acessá-los em versões anteriores é um benefício significativo para você como desenvolvedor.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Nosso convite para você como desenvolvedor DirectWrite

DWriteCore, juntamente com outros componentes de reunião do projeto, serão desenvolvidos com a abertura para comentários do desenvolvedor. Convidamos você a começar a explorar o DWriteCore e a fornecer ideias ou solicitações ao desenvolvimento de recursos em nosso [repositório GitHub de reunião do projeto](https://github.com/microsoft/ProjectReunion/).

## <a name="programming-with-dwritecore"></a>Programando com DWriteCore

Assim como com o [DirectWrite](./direct-write-portal.md), você programa com DWriteCore por meio de sua API com-Light, por meio da interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

Para usar o DWriteCore, é necessário incluir o `dwrite_core.h` arquivo de cabeçalho.

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

O `dwrite_core.h` arquivo de cabeçalho primeiro define o token *DWRITE_CORE* e, em seguida, inclui o `dwrite_3.h` arquivo de cabeçalho. O token *DWRITE_CORE* é importante, pois ele direciona quaisquer cabeçalhos incluídos subsequentemente para disponibilizar todas as APIs DirectWrite para você. Depois que o projeto tiver sido incluído `dwrite_core.h` , você poderá continuar e escrever código, criar e executar.

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>APIs que são novas ou diferentes para DWriteCore

A superfície da API do DWriteCore é basicamente a mesma que se trata de [DirectWrite](/windows/win32/api/_directwrite/). Mas há um pequeno número de novas APIs que só estão em DWriteCore no presente.

#### <a name="create-a-factory-object"></a>Criar um objeto de fábrica

A função Free [**DWriteCoreCreateFactory**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) cria um objeto de fábrica que é usado para a criação subsequente de objetos DWriteCore individuais.

**DWriteCoreCreateFactory** é funcionalmente o mesmo que a função [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada pela versão do sistema do DirectWrite. A função DWriteCore tem um nome diferente para evitar ambigüidade.

#### <a name="create-a-restricted-factory-object"></a>Criar um objeto de fábrica restrito

A enumeração de [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) tem uma nova constante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, indicando uma fábrica restrita. Uma fábrica restrita é mais bloqueada do que uma fábrica isolada. Ele não interage com um cache de fontes entre processos e persistentes de nenhuma forma. Além disso, a coleção de fontes do sistema retornada por essa fábrica inclui apenas fontes conhecidas. Veja como você pode usar **DWRITE_FACTORY_TYPE_ISOLATED2** para criar um objeto de fábrica restrito ao chamar a função gratuita [**DWriteCoreCreateFactory**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) .

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

Se você passar **DWRITE_FACTORY_TYPE_ISOLATED2** para uma versão mais antiga do DirectWrite que não ofereça suporte a ela, **DWriteCreateFactory** retornará **E_INVALIDARG**.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Glifos de desenho para um bitmap de memória do sistema

DirectWrite tem uma interface de destino de renderização de bitmap que dá suporte à renderização de glifos em um bitmap na memória do sistema. No entanto, atualmente a única maneira de obter acesso aos dados de pixel subjacentes é passar pelo GDI e, portanto, a API não é utilizável entre plataformas. Isso é facilmente remediado com a adição de um método para recuperar os dados de pixel.

Portanto, DWriteCore apresenta a interface [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) e seu método [**IDWriteBitmapRenderTarget2:: getbitmapdata**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md). Esse método usa um parâmetro de tipo (ponteiro para) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), que é uma nova estrutura.

Seu aplicativo cria um destino de renderização de bitmap chamando [IDWriteGdiInterop:: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). No Windows, um destino de renderização de bitmap encapsula um controlador de domínio de memória GDI com um bitmap independente de dispositivo (DIB) do GDI selecionado. [IDWriteBitmapRenderTarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) processa glifos para o DIB. DirectWrite renderiza os glifos em si sem passar pela GDI. Em seguida, seu aplicativo pode obter o **HDC** do destino de renderização de bitmap e usar [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar os pixels para uma janela **HDC**.

Em plataformas não Windows, seu aplicativo ainda pode criar um destino de renderização de bitmap, mas simplesmente encapsula uma matriz de memória do sistema sem **HDC** e sem DIB. Sem um **HDC**, precisa haver outra maneira de seu aplicativo obter os pixels de bitmap para que ele possa copiá-los ou usá-los de outra forma. Mesmo no Windows, às vezes é útil obter os dados reais do pixel, e mostramos a maneira atual de fazer isso no exemplo de código abaixo.

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>Outras diferenças de API entre DWriteCore e DirectWrite

Há algumas APIs que são apenas stubs ou que se comportam de maneira um pouco diferente em plataformas que não são do Windows. Por exemplo, [IDWriteGdiInterop:: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) retorna **E_NOTIMPL** em plataformas não Windows, já que não há tal coisa como um **HDC** sem [GDI](../gdi/windows-gdi.md).

E, finalmente, existem algumas outras APIs do Windows que normalmente são usadas junto com DirectWrite (Direct2D sendo um exemplo notável). No entanto, atualmente, Direct2D e DWriteCore não interoperam. Por exemplo, se você criar um [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando DWriteCore e passá-lo para [**D2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), essa chamada falhará.
