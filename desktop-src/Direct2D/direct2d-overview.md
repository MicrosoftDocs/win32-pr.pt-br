---
title: Sobre Direct2D
description: Apresenta Direct2D, uma API que fornece aos desenvolvedores do Win32 a capacidade de executar tarefas de renderização de gráficos 2D com desempenho superior e qualidade visual.
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D, sobre
- Direct2D, interoperabilidade
- Direct2D, desempenho
- Direct2D, disponibilidade
- Direct2D,aplicativos
- interoperabilidade, Direct2D
- desempenho para Direct2D
- disponibilidade para Direct2D
- aplicativos para Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe011b2d61fbb116efa4818f0db988d24e39fcb707e3ae42ddc0fb91f065652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825569"
---
# <a name="about-direct2d"></a>Sobre Direct2D

Este tópico apresenta Direct2D, uma API que fornece aos desenvolvedores do Win32 a capacidade de executar tarefas de renderização de gráficos 2D com desempenho superior e qualidade visual.

## <a name="what-is-direct2d"></a>O que é Direct2D?

Direct2D é uma API de gráficos 2D acelerada por hardware e modo imediato que fornece renderização de alto desempenho e alta qualidade para geometria, bitmaps e texto 2D. A API Direct2D é projetada para interoperar com o código existente que usa GDI, GDI+ ou Direct3D.

Direct2D é projetado principalmente para uso pelas seguintes classes de desenvolvedores:

-   Desenvolvedores de aplicativos nativos de grande escala empresarial.
-   Desenvolvedores que criam bibliotecas e kits de ferramentas de controle para consumo por desenvolvedores downstream.
-   Desenvolvedores que exigem renderização do lado do servidor de gráficos 2D.
-   Os desenvolvedores que usam gráficos Direct3D e precisam de renderização de texto 2D simples e de alto desempenho para menus, elementos de interface do usuário e HUDs (exibições de cabeça).

## <a name="why-direct2d"></a>Por que Direct2D?

As principais motivações para criar uma nova API de gráficos 2D no Microsoft Windows incluem o seguinte:

-   Para acompanhar o nível crescente de richness visual ao qual Windows usuários estão acostumados.
-   Para permitir que os desenvolvedores escrevam código de renderização 2D que é dimensionado diretamente com o hardware de processamento gráfico do computador em que ele está sendo executado.
-   Para permitir que os desenvolvedores escrevam código para renderizar gráficos 2D que podem ser executados no contexto de um serviço.

Nos últimos anos, os usuários finais começaram a esperar maior fidelidade visual em experiências digitais. Essa tendência é refletida em eletrônicos do consumidor. Dispositivos GPS, dispositivos de reprodução de mídia, celulares e câmeras digitais oferecem experiências consistentemente mais rica ano após ano. Essa tendência também pode ser vista na diversidade de conteúdo gráfico em filmes, tv, jogos de vídeo e na Web. Para acompanhar essas alterações, os desenvolvedores são constantemente solicitados a levar seus aplicativos Windows existentes para o próximo nível de richness visual.

Os processadores gráficos em PCs Windows modernos também foram evoluindo de forma constante, impulsionados por avanços em elementos gráficos de jogos de vídeo e partes da experiência de Windows, como o Windows Media Center e o Aero. Alguns Windows aplicativos podem aproveitar GPUs modernas usando o Microsoft Direct3D e Windows Presentation Foundation (WPF). Embora o Direct3D atende a aplicativos gráficos 3D de alto nível e o WPF atende às necessidades dos desenvolvedores do .NET, há lacunas para desenvolvedores que têm grandes bases de código existentes de código de renderização com base em GDI e GDI+ ou que querem incorporar gráficos 2D de alta qualidade em seus aplicativos baseados em Direct3D.

Por fim, a necessidade de uma API de gráficos que pode ser usada em um serviço tornou-se um requisito emergente para desenvolvedores que trabalham em cenários de desenvolvimento na Web e empresariais. As APIs de renderização existentes se concentram na renderização do lado do cliente em uma única sessão de usuário. Assim, eles podem ficar aquém em áreas de robustez e escalabilidade quando usadas em um contexto de serviço. Uma nova API é necessária para resolver isso.

## <a name="high-performance-with-maximum-availability"></a>Alto desempenho com disponibilidade máxima

Direct2D é uma biblioteca de modo de usuário criada usando a API do Direct3D 10.1. Isso significa que Direct2D aplicativos se beneficiam da renderização acelerada por hardware em GPUs tradicionais modernas. A aceleração de hardware também é alcançada em hardware Direct3D 9 anterior usando a renderização direct3D 10-level-9. Essa combinação fornece um excelente desempenho em hardware de gráficos em PCs Windows existentes.

> [!Note]  
> A partir Windows 8, o Direct2D é criado usando a API do Direct3D 11.1.

 

O diagrama a seguir mostra a arquitetura em camadas Direct2D.

![diagrama da arquitetura em camadas direct2d](images/direct2d-architectual-layering.png)

Para cenários em que o uso da aceleração de hardware não é viável, o Direct2D inclui um rasterizador de software de alto desempenho. Ao renderizar no software, os aplicativos que usam Direct2D têm um desempenho de renderização substancialmente melhor do que com GDI+ e com qualidade visual semelhante. O rasterizador de software também foi projetado para uso em um contexto de serviço.

O conteúdo renderizado usando Direct2D também pode ser exibido remotamente usando a infraestrutura RDP (protocolo RDP) no sistema operacional Windows 7. Os desenvolvedores podem selecionar se a renderização é manipulada pela GPU no computador de exibição ou renderizada localmente e transmitida como bitmaps. Essa escolha pode ser feita com base na taxa de preenchimento necessária e na quantidade de primitivos gráficos renderizados. Quando o computador de exibição está executando um sistema operacional anterior ao Windows 7, a renderização de exibição remota é executada transmitindo bitmaps pela rede.

Ao fornecer uma única API que combina o desempenho do Direct3D e alta disponibilidade fornecendo fallback de software, área de trabalho remota e renderização de serviço, o Direct2D permite que os desenvolvedores tenham uma única implementação para renderização de alto desempenho em muitos cenários diferentes.

## <a name="visual-quality"></a>Qualidade visual

Aplicativos que usam Direct2D gráficos podem fornecer uma qualidade visual maior do que a que pode ser obtido usando gDI. Direct2D usa suavização por primitivo para fornecer curvas de aparência mais suaves e linhas no conteúdo renderizado. Também há suporte completo para transparência e mesclagem alfa ao renderizar primitivos 2D. As imagens a seguir comparam o conteúdo com alias renderizado usando GDI (à esquerda) com o conteúdo suavizado renderizado por Direct2D (à direita).

![ilustração de curvas e linhas renderizadas em gdi e em direct2d](images/rendering-curves-and-lines.png)

Os desenvolvedores podem especificar a renderização com alias de elementos gráficos vetoriais. Isso é usado em cenários em que o ajuste a limites de pixel rígido é necessário, como elementos de interface do usuário, como ponteiros ou réguas, se o estilo GDI de saída deve ser corresponder ou se a antialização será executada downstream no processo de renderização por meio de Antialização multisample ou algum outro mecanismo.

## <a name="interoperability"></a>Interoperabilidade

A integração Direct2D renderização baseada em dados fica mais fácil para os desenvolvedores por meio da interoperabilidade no nível da superfície com GDI e Direct3D. Aplicativos que renderizam conteúdo principalmente com GDI, GDI+ ou Direct3D, podem começar usando o Direct2D para renderizar áreas específicas de seu aplicativo e, ao longo do tempo, mudar para um modelo em que a renderização é executada principalmente por meio do Direct2D, usando a GDI principalmente para plug-ins ou extensibilidade herdada.

Direct2D também facilita o uso do [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para texto de alta qualidade e os recursos avançados de imagens do [WIC (Microsoft Windows Imaging Component).](https://msdn.microsoft.com/library/ms737408.aspx)

Para obter mais informações Direct2D interoperabilidade, consulte a seção [Interoperabilidade do SDK do Direct2D.](interoperability.md)

## <a name="summary"></a>Resumo

O Microsoft Direct2D permite que os desenvolvedores criem recursos gráficos 2D em seus aplicativos que oferecem qualidade visual aprimorada em relação à GDI e características de desempenho que são dimensionados com GPUs modernas. O Direct2D de interoperabilidade permite que os desenvolvedores migrem seletivamente partes de seu aplicativo por vez junto com a renderização baseada em GDI, GDI+ ou Direct3D.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Início Rápido para Windows 8](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Visão geral de API do Direct2D](the-direct2d-api.md)
</dt> </dl>

 

 