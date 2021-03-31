---
title: Sobre o Direct2D
description: Apresenta o Direct2D, uma API que fornece aos desenvolvedores do Win32 a capacidade de executar tarefas de renderização de gráficos 2D com desempenho e qualidade visual superiores.
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D, sobre
- Direct2D, interoperabilidade
- Direct2D, desempenho
- Direct2D, disponibilidade
- Direct2D, aplicativos
- interoperabilidade, Direct2D
- desempenho para Direct2D
- disponibilidade para Direct2D
- aplicativos para Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486c83b7a83ef82983e189977f9f99254b0a1977
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917507"
---
# <a name="about-direct2d"></a>Sobre o Direct2D

Este tópico apresenta o Direct2D, uma API que fornece aos desenvolvedores do Win32 a capacidade de executar tarefas de renderização de gráficos 2D com desempenho e qualidade visual superiores.

## <a name="what-is-direct2d"></a>O que é o Direct2D?

O Direct2D é uma API de gráficos de modo imediato de hardware e 2-D que fornece alto desempenho e renderização de alta qualidade para geometria, bitmaps e texto 2D. A API Direct2D foi projetada para interoperar com o código existente que usa GDI, GDI+ ou Direct3D.

O Direct2D é projetado principalmente para uso pelas seguintes classes de desenvolvedores:

-   Desenvolvedores de aplicativos nativos de grande escala empresarial.
-   Desenvolvedores que criam kits de controle e bibliotecas para consumo por desenvolvedores de downstream.
-   Desenvolvedores que exigem renderização do lado do servidor de gráficos 2D.
-   Os desenvolvedores que usam gráficos do Direct3D e precisam de renderização simples, de alto desempenho em 2 e de texto para menus, elementos da interface do usuário (UI) e HUDs (exibições de cabeçotes).

## <a name="why-direct2d"></a>Por que Direct2D?

As principais motivações para a criação de uma nova API de gráficos 2D no Microsoft Windows incluem o seguinte:

-   Para acompanhar o crescimento do nível de riqueza visual de que os usuários do Windows estão acostumados.
-   Para permitir que os desenvolvedores escrevam código de renderização 2D que seja dimensionado diretamente com o hardware de processamento de gráficos do computador em que ele está sendo executado.
-   Para permitir que os desenvolvedores escrevam código para renderização de elementos gráficos 2D que podem ser executados no contexto de um serviço.

Nos últimos anos, os usuários finais começaram a esperar uma maior fidelidade visual em experiências digitais. Essa tendência é refletida na eletrônica de consumidores. Dispositivos GPS, dispositivos de reprodução de mídia, celulares e câmeras digitais entregam anos de experiências consistentemente mais ricos após o ano. Essa tendência também pode ser vista na diversidade de conteúdo gráfico em filmes, televisão, jogos de vídeo e na Web. Para acompanhar essas alterações, os desenvolvedores são constantemente solicitados a levar seus aplicativos Windows existentes para o próximo nível de riqueza visual.

Os processadores gráficos em PCs Windows modernos também foram evoluindo constantemente, orientados por avanços em gráficos de jogos de vídeo e por partes da experiência do Windows, como Windows Media Center e Aero. Alguns aplicativos do Windows podem aproveitar as GPUs modernas usando o Microsoft Direct3D e o Windows Presentation Foundation (WPF). Embora o Direct3D sirva aplicativos gráficos 3D avançados e o WPF atenda às necessidades dos desenvolvedores do .NET, há lacunas para os desenvolvedores que têm grandes bases de código de renderização com base em GDI e GDI+ ou que desejam incorporar gráficos de alta qualidade 2D em seus aplicativos baseados em Direct3D.

Por fim, a necessidade de uma API gráfica que possa ser usada em um serviço tornou-se um requisito emergente para os desenvolvedores que trabalham em cenários empresariais e de desenvolvimento na Web. As APIs de renderização existentes se concentram na renderização do lado do cliente em uma única sessão de usuário. Assim, eles podem cair em áreas de robustez e escalabilidade quando usados em um contexto de serviço. Uma nova API é necessária para resolver isso.

## <a name="high-performance-with-maximum-availability"></a>Alto desempenho com disponibilidade máxima

Direct2D é uma biblioteca de modo de usuário que é criada usando a API do Direct3D 10,1. Isso significa que aplicativos Direct2D se beneficiam da renderização acelerada por hardware em GPUs convencionais modernas. A aceleração de hardware também é obtida em hardware do Direct3D 9 anterior usando a renderização Direct3D 10-Level-9. Essa combinação fornece excelente desempenho em hardware de gráficos em computadores Windows existentes.

> [!Note]  
> A partir do Windows 8, o Direct2D é criado usando a API do Direct3D 11,1.

 

O diagrama a seguir mostra a arquitetura em camadas do Direct2D.

![diagrama da arquitetura em camadas Direct2D](images/direct2d-architectual-layering.png)

Para cenários em que o uso da aceleração de hardware não é viável, o Direct2D inclui um rasterizador de software de alto desempenho. Ao renderizar no software, os aplicativos que usam a experiência de Direct2D de forma substancialmente melhoram o desempenho do que com o GDI+ e com uma qualidade visual semelhante. O rasterizador de software também foi projetado para uso em um contexto de serviço.

O conteúdo que é processado usando Direct2D também pode ser exibido remotamente usando a infraestrutura protocolo RDP (RDP) no sistema operacional Windows 7. Os desenvolvedores podem selecionar se a renderização é tratada pela GPU no computador de exibição ou renderizada localmente e transmitida como bitmaps. Essa opção pode ser feita com base na taxa de preenchimento necessária e na quantidade de primitivos gráficos que são renderizados. Quando o computador de vídeo está executando um sistema operacional anterior ao Windows 7, a renderização de exibição remota é executada pela transmissão de bitmaps pela rede.

Ao fornecer uma única API que combina o desempenho do Direct3D e da alta disponibilidade ao fornecer fallback de software, área de trabalho remota e renderização de serviço, o Direct2D permite que os desenvolvedores tenham uma única implementação para renderização de alto desempenho em vários cenários diferentes.

## <a name="visual-quality"></a>Qualidade visual

Os aplicativos que usam o Direct2D para gráficos podem fornecer uma qualidade visual maior do que o que pode ser obtido usando GDI. O Direct2D usa a suavização por primitiva para fornecer curvas e linhas de aparência mais suaves no conteúdo renderizado. Também há suporte completo para transparência e mesclagem alfa ao renderizar primitivos 2-D. As imagens a seguir comparam o conteúdo com alias renderizado usando GDI (à esquerda) com conteúdo com suavização de alias renderizado por Direct2D (à direita).

![ilustração de curvas e linhas que são renderizadas em GDI e em Direct2D](images/rendering-curves-and-lines.png)

Os desenvolvedores podem especificar a renderização com alias de gráficos vetoriais. Isso é usado em cenários em que é necessário ajustar a limites de pixel rígido, como elementos de interface do usuário, como ponteiros ou réguas, se o estilo de saída GDI deve ser correspondido ou se a anti-aliasing for executada no processo de renderização por meio de anti-aliasing de multiamostra ou de algum outro mecanismo.

## <a name="interoperability"></a>Interoperabilidade

A integração da renderização baseada em Direct2D é mais fácil para os desenvolvedores por meio da interoperabilidade no nível da superfície com GDI e Direct3D. Os aplicativos que renderizam o conteúdo principalmente com GDI, GDI+ ou Direct3D podem começar usando Direct2D para renderizar áreas específicas de seu aplicativo e, ao longo do tempo, passar para um modelo em que a renderização é realizada principalmente por meio do Direct2D, usando a GDI principalmente para plug-ins ou extensibilidade herdada.

O Direct2D também facilita o uso de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para texto de alta qualidade e os recursos avançados de geração de imagens do [Microsoft Windows Imaging Component (WIC)](https://msdn.microsoft.com/library/ms737408.aspx).

Para obter mais informações sobre a interoperabilidade do Direct2D, consulte a [seção interoperabilidade do SDK do Direct2D.](interoperability.md)

## <a name="summary"></a>Resumo

O Microsoft Direct2D permite que os desenvolvedores criem recursos gráficos 2D em seus aplicativos que fornecem qualidade visual aprimorada sobre GDI e características de desempenho que são dimensionadas com GPUs modernas. O modelo de interoperabilidade Direct2D permite que os desenvolvedores migrem de forma seletiva partes de seu aplicativo de cada vez juntamente com a renderização GDI, GDI+ ou Direct3D.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de início rápido do Direct2D para Windows 8](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Visão geral de API do Direct2D](the-direct2d-api.md)
</dt> </dl>

 

 