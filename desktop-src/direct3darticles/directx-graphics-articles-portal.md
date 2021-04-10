---
title: Artigos sobre elementos gráficos do DirectX
description: .
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ac2a3a6b9beff7dfc8bfe4f6c0de92885f39ca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294354"
---
# <a name="directx-graphics-articles"></a>Artigos sobre elementos gráficos do DirectX

## <a name="purpose"></a>Finalidade

Esta seção contém artigos técnicos que descrevem o suporte recém-adicionado à WARP e ao Windows 7 para o modo flip presente e suas estatísticas atuais associadas no Direct3D 9Ex e Gerenciador de Janelas da Área de Trabalho. Esta seção também contém artigos técnicos sobre as APIs de gráficos do Windows, portando APIs do Direct3D 9 para APIs do Microsoft DirectX Graphics Infrastructure (DXGI) e como implantar o Direct3D 11.

Para obter mais informações sobre o Direct3D, consulte [Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Público de desenvolvedores

Esses artigos técnicos são para desenvolvedores de aplicativos de elementos gráficos do DirectX.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [Atualização de plataforma para o Windows 7](platform-update-for-windows-7.md) | Descreve quais componentes da pilha gráfica do Windows 8 se tornam disponíveis e em que ponto, por meio da [atualização da plataforma para o Windows 7](https://support.microsoft.com/kb/2670838). |
| [Aprimoramentos do Direct3D 9Ex](direct3d-9ex-improvements.md) | Descreve o suporte recém-adicionado ao Windows 7 para o modo flip e suas estatísticas atuais associadas no Direct3D 9Ex e Gerenciador de Janelas da Área de Trabalho. Os aplicativos de destino incluem aplicativos de apresentação baseados em vídeo ou em taxa de quadros. Os aplicativos que usam o modo de flip do Direct3D 9Ex presente reduzem a carga de recursos do sistema quando o DWM está habilitado. As melhorias de estatísticas atuais associadas ao modo Inverter apresentam a habilitação dos aplicativos do Direct3D 9Ex para controlar melhor a taxa de apresentação, fornecendo comentários em tempo real e mecanismos de correção. São incluídas explicações e ponteiros detalhados para recursos de exemplo. |
| [Compartilhamento de superfície entre as APIs de gráficos do Windows](surface-sharing-between-windows-graphics-apis.md) | Fornece uma visão geral técnica da interoperabilidade usando o compartilhamento de superfície entre as APIs de gráficos do Windows, incluindo Direct3D 11, Direct2D, Direct3D 10 e Direct3D 9Ex. Se você já tiver um conhecimento prático dessas APIs, este documento poderá ajudá-lo a usar várias APIs para renderizar a mesma superfície em um aplicativo projetado para os sistemas operacionais Windows 7 ou Windows Vista. Este tópico também fornece diretrizes de práticas recomendadas e ponteiros para recursos adicionais. |
| [Guia de detorção](directx-warp.md) | Fornece um guia da WARP (plataforma de rasterização avançada do Windows), um rasterizador de software de alta velocidade. |
| [APIs de gráficos no Windows](graphics-apis-in-windows-vista.md) | Discute os recursos e as APIs de gráficos do Windows. |
| [Implantação do Direct3D 11 para desenvolvedores de jogos](direct3d11-deployment.md) | Descreve como implantar os componentes do Direct3D 11 em um sistema. |
| [DXGI (infra-estrutura de gráficos do DirectX): práticas recomendadas](dxgi-best-practices.md) | Discute problemas sobre a portabilidade de APIs do Direct3D 9 para APIs e recursos do DXGI de várias versões do DXGI. |
| [Usar DirectX com exibições de alto alcance dinâmico e cor avançada](high-dynamic-range.md) | Este tópico fornece uma visão geral técnica da renderização do conteúdo do Direct3D 11 e do Direct3D 12 de intervalo dinâmico para uma exibição HDR10 usando o suporte a cores avançadas do Windows 10. |