---
description: Introdução aos elementos gráficos do DirectX
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Introdução aos elementos gráficos do DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c5e8cca9f0cea4c1c5e484ba330c7c108cad40
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117584"
---
# <a name="getting-started-with-directx-graphics"></a>Introdução aos elementos gráficos do DirectX

O Microsoft DirectX Graphics fornece um conjunto de APIs que você pode usar para criar jogos e outros aplicativos multimídia de alto desempenho. O DirectX Graphics inclui suporte para gráficos 2D e 3D de alto desempenho.

Para gráficos 3D, use a API do Microsoft Direct3D 11. Mesmo que você tenha um hardware de nível do Microsoft Direct3D 9 ou Microsoft Direct3D 10, você pode usar a API do Direct3D 11 e ter como [destino um](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) dispositivo de nível de recurso 9 \_ x ou de nível de recurso 10 \_ x. Para obter informações sobre como desenvolver gráficos 3D com o DirectX, consulte [criar gráficos 3D com o DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).

Para gráficos e texto 2D, use Direct2D e [DirectWrite](./directwrite/direct-write-portal.md) em vez do Windows Graphics Device Interface (GDI).

Para compor os bitmaps que o Direct3D 11 ou o Direct2D populau, use [DirectComposition](./directcomp/directcomposition-portal.md).

Para saber mais sobre como criar um aplicativo da Windows Store que usa o DirectX, consulte [criar seu primeiro aplicativo da Windows Store usando o DirectX](/previous-versions/windows/apps/br229580(v=win.10)
). Você pode usar a classe [**Windows. UI:: XAML:: Controls:: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) para criar aplicativos DirectX de alto desempenho com uma sobreposição de interface do usuário XAML. Para obter mais informações sobre como combinar XAML e DirectX em um aplicativo do Windows, consulte [DirectX e interoperabilidade XAML](/previous-versions/windows/apps/hh825871(v=win.10)).

Para saber mais sobre como criar um driver de vídeo para o Windows 8, consulte [o roteiro para o Windows Display Driver Model (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).

Se precisar da documentação para versões anteriores do DirectX, consulte [elementos gráficos do DirectX clássico](/windows/desktop/classic-directx-graphics).


 

 
