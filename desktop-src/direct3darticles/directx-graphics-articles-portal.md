---
title: Artigos sobre elementos gráficos do DirectX
description: Artigos sobre elementos gráficos do DirectX
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5562b4b7dafc899d1c6a827cfd2e240a20013be7a31f225cdd41893d967748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095496"
---
# <a name="directx-graphics-articles"></a>Artigos sobre elementos gráficos do DirectX

## <a name="purpose"></a>Finalidade

esta seção contém artigos técnicos que descrevem o suporte recém-adicionado à deformação e à Windows 7 para o modo invertido presente e suas estatísticas atuais associadas no Direct3D 9ex e Gerenciador de Janelas da Área de Trabalho. esta seção também contém artigos técnicos sobre Windows apis de gráficos, portando apis do Direct3D 9 para apis do Microsoft DirectX graphics Infrastructure (DXGI) e como implantar o Direct3D 11.

Para obter mais informações sobre o Direct3D, consulte [Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Público de desenvolvedores

Esses artigos técnicos são para desenvolvedores de aplicativos de elementos gráficos do DirectX.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [atualização da plataforma para o Windows 7](platform-update-for-windows-7.md) | descreve quais componentes da pilha de gráficos de Windows 8 se tornam disponíveis e em que ponto, por meio da [atualização de plataforma para Windows 7](https://support.microsoft.com/kb/2670838). |
| [Aprimoramentos do Direct3D 9Ex](direct3d-9ex-improvements.md) | descreve o suporte recém-adicionado de Windows 7 para o modo Flip presente e suas estatísticas atuais associadas no Direct3D 9ex e Gerenciador de Janelas da Área de Trabalho. Os aplicativos de destino incluem aplicativos de apresentação baseados em vídeo ou em taxa de quadros. Os aplicativos que usam o modo de flip do Direct3D 9Ex presente reduzem a carga de recursos do sistema quando o DWM está habilitado. As melhorias de estatísticas atuais associadas ao modo Inverter apresentam a habilitação dos aplicativos do Direct3D 9Ex para controlar melhor a taxa de apresentação, fornecendo comentários em tempo real e mecanismos de correção. São incluídas explicações e ponteiros detalhados para recursos de exemplo. |
| [Compartilhamento de superfície entre as APIs de gráficos do Windows](surface-sharing-between-windows-graphics-apis.md) | fornece uma visão geral técnica da interoperabilidade usando o compartilhamento de superfície entre Windows APIs de gráficos, incluindo direct3d 11, Direct2D, direct3d 10 e direct3d 9ex. se você já tiver um conhecimento prático dessas APIs, este documento poderá ajudá-lo a usar várias apis para renderizar a mesma superfície em um aplicativo projetado para os sistemas operacionais Windows 7 ou Windows Vista. Este tópico também fornece diretrizes de práticas recomendadas e ponteiros para recursos adicionais. |
| [Guia de detorção](directx-warp.md) | fornece um guia de Windows a WARP (plataforma de rasterização avançada), um rasterizador de software de alta velocidade. |
| [APIs de gráficos no Windows](graphics-apis-in-windows-vista.md) | discute Windows recursos gráficos e APIs. |
| [Implantação do Direct3D 11 para desenvolvedores de jogos](direct3d11-deployment.md) | Descreve como implantar os componentes do Direct3D 11 em um sistema. |
| [DXGI (infra-estrutura de gráficos do DirectX): práticas recomendadas](dxgi-best-practices.md) | Discute problemas sobre a portabilidade de APIs do Direct3D 9 para APIs e recursos do DXGI de várias versões do DXGI. |
| [Usar DirectX com exibições de alto alcance dinâmico e cor avançada](high-dynamic-range.md) | este tópico fornece uma visão geral técnica da renderização do conteúdo do direct3d 11 e do direct3d 12 de intervalo dinâmico para uma exibição HDR10 usando Windows 10 suporte a cores avançado. |
