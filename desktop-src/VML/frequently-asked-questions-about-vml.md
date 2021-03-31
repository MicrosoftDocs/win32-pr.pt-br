---
title: Perguntas frequentes sobre a VML
description: Perguntas frequentes sobre a VML
ms.assetid: f7f2ce12-facf-4042-b2a7-acaa3e25816a
keywords:
- Linguagem VML (VML), perguntas frequentes
- VML (linguagem VML), perguntas frequentes
- gráficos vetoriais, perguntas frequentes
- Linguagem VML (VML), perguntas frequentes
- VML (linguagem VML), perguntas frequentes
- gráficos vetoriais, perguntas frequentes
- Linguagem VML (VML), diferenças de GIF
- VML (linguagem VML), diferenças de GIF
- Linguagem VML (VML), diferenças de PNG
- VML (linguagem VML), diferenças de PNG
- gráficos vetoriais, diferenças de formato de rasterização
- Linguagem VML (VML), XML
- VML (linguagem VML), XML
- gráficos vetoriais, XML
- Linguagem VML (VML), animação
- VML (linguagem VML), animação
- gráficos vetoriais, animação
- Linguagem VML (VML), Macromedia Flash
- VML (linguagem VML), Macromedia Flash
- gráficos vetoriais, Macromedia Flash
- formatos de rasterização
- animação
- Flash da Macromedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e108f2055e7a0fbae1c5ed542fe68c59ec9b212b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917518"
---
# <a name="frequently-asked-questions-about-vml"></a>Perguntas frequentes sobre a VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

## <a name="does-vml-compete-with-gif-and-png"></a>A VML é concorrente com GIF e PNG?

Não. GIF e PNG são formatos rasterizados (ou mapeados por bits) que podem ser usados para armazenar gráficos vetoriais. Os formatos de varredura armazenam cada pixel, enquanto que os formatos de vetor, como VML, usam descrições matemáticas ou contornos para descrever os gráficos. Os gráficos vetoriais armazenados em um formato baseado em vetor são mais compactados do que aqueles armazenados em formatos de varredura, resultando em tempos de download mais rápidos para usuários da Web.

Além disso, os elementos gráficos VML são entregues embutidos na página HTML em vez de depender de arquivos externos, como é o caso com GIF e PNG hoje. Isso permite que elementos gráficos VML sejam dimensionados e interajam com outros elementos da página da Web à medida que a página é redimensionada, melhorando assim a experiência do usuário final.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a>Por que a Microsoft dá suporte a outro padrão baseado em XML quando o XML dificilmente está em uso e é jovem o suficiente como é?

O XML é uma maneira poderosa, mas simples, de representar dados estruturados na Web e complementa totalmente o HTML para exibição. A VML é um exemplo dos muitos formatos baseados em XML, específicos do aplicativo que serão desenvolvidos e implementados nos próximos meses. Por exemplo, na próxima versão do Office, a VML será usada para anotar documentos HTML – para preservar as informações de formatação dos gráficos de arte do Office entre o formato de arquivo nativo do Office e o HTML, permitindo que os usuários do Office alternem diretamente entre os dois formatos.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="who-will-support-vml"></a>Quem dará suporte a VML?

Esperamos que muitos fornecedores ofereçam suporte a VML. Por exemplo, Autodesk, Hewlett-Packard, Macromedia e VISIO têm suporte de VML em versões futuras de seus produtos. A Microsoft penhorou o suporte para VML em versões futuras de suas plataformas, como o Internet Explorer. Além disso, o VML será usado na próxima geração do Office para habilitar "ida e volta" entre o formato do Office e o HTML.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="does-vml-support-animation"></a>A VML dá suporte à animação?

Não, atualmente não. No entanto, estamos trabalhando com nossos parceiros de VML para adicionar capacidade de animação no formato VML. Como a VML é baseada em XML, o conjunto de marcas pode ser facilmente estendido para funcionalidade adicional.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a>A VML substitui o Macromedia Flash? Não a Macromedia não enviasse apenas seu formato Flash para gráficos vetoriais para o W3C?

Não. A VML é um formato de entrega e distribuição baseado em texto para gráficos vetoriais, enquanto o flash é um formato binário para a entrega de gráficos e animações baseados em vetores.

A Macromedia não enviou seu formato de arquivo para o W3C. No entanto, eles abriram seu formato de arquivo para desenvolvedores de aplicativos, desenvolvedores da Web e usuários finais. Consulte <https://www.macromedia.com> para obter mais informações.

[Voltar para a visão geral da VML](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 