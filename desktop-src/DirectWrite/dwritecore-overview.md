---
title: Visão geral do DWriteCore
description: DWriteCore é a implementação do SDK do Aplicativo do Windows do DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: a537d26f6aca4e2be64b61fd41da91e1f8829894
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587778"
---
# <a name="dwritecore-overview"></a>Visão geral do DWriteCore

DWriteCore é a implementação do [SDK](/windows/apps/windows-app-sdk/) do Aplicativo do Windows [do DirectWrite (DirectWrite](./direct-write-portal.md) é a API do DirectX para renderização de texto de alta qualidade, fontes de estrutura de contorno independentes de resolução e suporte completo a texto e layout Unicode). DWriteCore é uma forma de DirectWrite que é executado em versões do Windows até Windows 10, versão 1809 (10.0; Build 17763) e abre a porta para você usá-lo em plataforma cruzada.

Este tópico introdutório descreve o que é o DWriteCore e mostra como instalá-lo em seu ambiente dev e programa com ele.

> [!TIP]
> Para ver descrições de e links para componentes do DirectX no desenvolvimento ativo, consulte a postagem no blog Página de aterrissagem [do DirectX](https://devblogs.microsoft.com/directx/landing-page/).

## <a name="the-value-proposition-of-dwritecore"></a>A proposta de valor de DWriteCore

[O DirectWrite](./direct-write-portal.md) em si dá suporte a uma ampla variedade de recursos que o torna a ferramenta de renderização de fonte de sua escolha no Windows para a maioria dos aplicativos, seja por meio de chamadas diretas ou por &mdash; meio do [Direct2D.](../direct2d/direct2d-portal.md) O DirectWrite inclui um sistema de layout de texto independente de dispositivo, renderização de texto [Microsoft ClearType](/typography/cleartype/) de sub pixel de alta qualidade, texto acelerado por hardware, texto de vários formatos, recursos avançados de [tipografia OpenType®](/typography/opentype/) suporte a linguagem ampla e layout e renderização compatíveis com [GDI.](../gdi/windows-gdi.md) O DirectWrite está disponível desde o Windows Vista SP2 e evoluiu ao longo dos anos para incluir recursos mais avançados, como fontes variáveis, o que permite aplicar estilos, pesos e outros atributos a uma fonte com apenas um recurso de fonte.

No entanto, devido ao longo período de vida do DirectWrite, os avanços no desenvolvimento tendem a deixar versões mais antigas do Windows para trás. Além disso, o status do DirectWrite como a tecnologia de renderização de texto premier é limitado apenas ao Windows, deixando aplicativos de plataforma cruzada escreverem sua própria pilha de renderização de texto ou dependerem de soluções de terceiros.

DWriteCore resolve os problemas fundamentais de compatibilidade de recursos de versão órfãos e multiplatafa removendo a biblioteca do sistema e direcionando todos os pontos de extremidade com suporte possíveis. Para esse fim, integramos o DWriteCore ao SDK de Aplicativos do Windows.

O principal valor que o DWriteCore fornece, como desenvolvedor, no SDK de Aplicativos do Windows é que ele fornece acesso a muitos (e, eventualmente, a todos) recursos directWrite. Todos os recursos do DWriteCore funcionarão da mesma forma em todas as versões de nível inferior sem qualquer disparidade sobre quais recursos podem funcionar em quais versões.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>O aplicativo de demonstração &mdash; DWriteCore DWriteCoreGallery

DWriteCore é demonstrado por meio do aplicativo de exemplo [DWriteCoreGallery,](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) que está disponível para download e estudo.

## <a name="get-started-with-dwritecore"></a>Começar a trabalhar com DWriteCore

O DWriteCore faz parte do [SDK de Aplicativos do Windows 0.8.](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0) Esta seção descreve como configurar seu ambiente de desenvolvimento para programação com DWriteCore.

### <a name="install-the-windows-app-sdk-08-vsix"></a>Instalar o VSIX do SDK do Aplicativo do Windows 0.8

No Visual Studio, **clique** em Extensões Gerenciar Extensões, pesquise  >  *SDK* de **Aplicativos** do Windows e baixe a extensão do SDK do Aplicativo do Windows. Feche e reabra Visual Studio e siga os prompts para instalar a extensão.

Para obter mais informações, consulte [SDK do Aplicativo do Windows 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0) [e Configurar seu ambiente de desenvolvimento](/windows/apps/windows-app-sdk/set-up-your-development-environment#3-install-the-windows-app-sdk-extension-for-visual-studio).

### <a name="create-a-new-project"></a>Criar um novo projeto

No Visual Studio, crie um novo projeto do modelo de projeto Aplicativo em **Branco, Empacotado (WinUI 3 na Área** de Trabalho). Você pode encontrar esse modelo de projeto escolhendo o idioma: *C++;* platform: *SDK do Aplicativo do Windows*; tipo de projeto: *Área de Trabalho.*

Para obter mais informações, consulte [Modelos de projeto para WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>Instalar o pacote NuGet Microsoft.ProjectReunion.DWrite

No Visual Studio, clique  em Projeto Gerenciar Pacotes NuGet... Procure , digite ou colar \>  \>  **Microsoft.ProjectReunion.DWrite**  na caixa de pesquisa, selecione o item nos resultados da pesquisa e clique em Instalar para instalar o pacote para esse projeto.

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>Como alternativa, comece com o aplicativo de exemplo DWriteCoreGallery

Como alternativa, você pode programar com DWriteCore começando com o projeto de aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) e basear seu desenvolvimento nesse projeto. Em seguida, você pode se sentir à vontade para remover qualquer código-fonte (ou arquivos) existente desse projeto de exemplo e adicionar qualquer novo código-fonte (ou arquivos) ao projeto.

### <a name="use-dwritecore-in-your-project"></a>Usar DWriteCore em seu projeto

Para obter mais informações sobre programação com DWriteCore, consulte a [seção Programação com DWriteCore](#programming-with-dwritecore) mais adiante neste tópico.

## <a name="the-release-phases-of-dwritecore"></a>As fases de lançamento do DWriteCore

Portar DirectWrite para DWriteCore é um projeto suficientemente grande para abranger vários ciclos de lançamento do Windows. Esse projeto é dividido em fases, cada uma correspondendo a uma parte da funcionalidade entregue em uma versão.

### <a name="features-in-the-current-release-of-dwritecore"></a>Recursos na versão atual do DWriteCore

A versão do DWriteCore atualmente disponível faz parte do SDK de Aplicativos [do Windows 0.8.](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0) Ele contém as ferramentas básicas que você, como desenvolvedor, precisa consumir DWriteCore, incluindo os recursos a seguir.

- Enumeração de fonte.
- API de fonte.
- Moldar.
- APIs de renderização de baixo nível. Isso é parcial na fase atual &mdash; O DWriteCore não interopera com [o Direct2D,](../direct2d/direct2d-portal.md)mas você pode usar [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).
- Funcionalidade básica de layout de texto.
- APIs de renderização de texto.
- Destino de renderização de bitmap.
- Fontes de cores.
- Otimizações diversas (limpeza de cache de fonte, carregador de fonte na memória e assim por diante).
- Suporte para &mdash; sublinhado consulte [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) e [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline).
- Suporte para tachado &mdash; consulte [**IDWriteTextLayout::GetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getstrikethrough) e [**IDWriteTextLayout::SetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setstrikethrough).
- Suporte para texto vertical por [**meio de IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) &mdash; consulte Texto [vertical](/windows/win32/directwrite/vertical-text).
- Todos os métodos das interfaces [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) e [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) são implementados.

Um recurso de faixa são fontes de cores. As fontes de cores permitem renderizar suas fontes com funcionalidades de cores mais sofisticadas além de cores simples. Por exemplo, fontes de cores é o que alimenta a capacidade de renderizar fontes de ícone de barra de ferramentas e emoji (a última das quais é usada pelo Office, por exemplo). As fontes de cores foram introduzidas pela primeira vez no Windows 8.1, mas o recurso foi muito expandido no Windows 10, versão 1607 (Atualização de Aniversário).

O trabalho na limpeza do cache de fontes e no carregador de fontes na memória permitem o carregamento mais rápido de fontes e aprimoramentos de memória.

Com esses recursos, você pode começar imediatamente a aproveitar algumas das funcionalidades básicas modernas do DirectWrite, como &mdash; fontes variáveis. Fontes de variável são um dos recursos mais importantes para clientes directWrite.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Nosso convite para você como desenvolvedor do DirectWrite

O DWriteCore, juntamente com outros componentes do SDK de Aplicativos do Windows, será desenvolvido com abertura para comentários dos desenvolvedores. Convidamos você a começar a explorar o DWriteCore e fornecer insights ou solicitações sobre o desenvolvimento de recursos em nosso repositório [GitHub do SDK](https://github.com/microsoft/ProjectReunion/)de Aplicativos do Windows.

## <a name="programming-with-dwritecore"></a>Programação com DWriteCore

Assim como no [DirectWrite](./direct-write-portal.md), você programa com DWriteCore por meio de sua API com luz COM, por meio da interface [**IDWriteFactory.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)

Para usar DWriteCore, é necessário incluir o `dwrite_core.h` arquivo de header.

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

O `dwrite_core.h` arquivo de título primeiro define o token *DWRITE_CORE* e, em seguida, inclui o arquivo `dwrite_3.h` de título. O *DWRITE_CORE* token é importante, pois ele direciona todos os headers subsequentemente incluídos para disponibilizar todas as APIs do DirectWrite para você. Depois que o projeto tiver incluído , você poderá continuar `dwrite_core.h` e escrever código, criar e executar.

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>APIs novas ou diferentes para DWriteCore

A superfície da API DWriteCore é a maior parte da mesma que é para [DirectWrite.](/windows/win32/api/_directwrite/) Mas há um pequeno número de novas APIs que estão apenas em DWriteCore no momento.

#### <a name="create-a-factory-object"></a>Criar um objeto de fábrica

A [**função livre DWriteCoreCreateFactory**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) cria um objeto de fábrica que é usado para a criação subsequente de objetos DWriteCore individuais.

**DWriteCoreCreateFactory** é funcionalmente o mesmo que a [função DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada pela versão do sistema do DirectWrite. A função DWriteCore tem um nome diferente para evitar ambiguidade.

#### <a name="create-a-restricted-factory-object"></a>Criar um objeto de fábrica restrito

A [**DWRITE_FACTORY_TYPE**](/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type) enumeração tem uma nova constante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, indicando uma fábrica restrita. Uma fábrica restrita é mais bloqueada do que uma fábrica isolada. Ele não interage com um cache de fontes persistente nem entre processos de forma alguma. Além disso, a coleção de fontes do sistema retornada dessa fábrica inclui apenas fontes conhecidas. Veja como você pode usar o **DWRITE_FACTORY_TYPE_ISOLATED2** criar um objeto de fábrica restrito ao chamar a função livre [**DWriteCoreCreateFactory.**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory)

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

Se você passar **DWRITE_FACTORY_TYPE_ISOLATED2** para uma versão mais antiga do DirectWrite que não dá suporte a ela, **DWriteCreateFactory** retornará **E_INVALIDARG**.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Desenhando glifos em um bitmap de memória do sistema

DirectWrite tem uma interface de destino de renderização de bitmap que dá suporte à renderização de glifos em um bitmap na memória do sistema. No entanto, atualmente, a única maneira de obter acesso aos dados de pixel subjacente é passar pela GDI e, portanto, a API não pode ser usada entre plataformas. Isso é facilmente corrigido adicionando um método para recuperar os dados de pixel.

Portanto, dWriteCore introduz a interface [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata) e seu método [**IDWriteBitmapRenderTarget2::GetBitmapData**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata). Esse método recebe um parâmetro do tipo (ponteiro para) [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32), que é um novo struct.

Seu aplicativo cria um destino de renderização de bitmap chamando [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). No Windows, um destino de renderização de bitmap encapsula um DC de memória GDI com um DIB (bitmap independente de dispositivo) GDI selecionado nele. [IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renderiza glifos para o DIB. DirectWrite renderiza os glifos em si sem passar pela GDI. Em seguida, seu aplicativo pode obter o **HDC** do destino de renderização de bitmap e usar [o BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar os pixels para um **HDC de janela.**

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
