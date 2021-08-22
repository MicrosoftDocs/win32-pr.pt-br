---
description: Introdução aos elementos gráficos do DirectX
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Introdução aos elementos gráficos do DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e0bc8a3485091ec8b8fa53c8245a3a4916e11af96493d4895585061f2b080f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830566"
---
# <a name="getting-started-with-directx-graphics"></a>Introdução aos elementos gráficos do DirectX

O Microsoft DirectX Graphics fornece um conjunto de APIs que você pode usar para criar jogos e outros aplicativos multimídia de alto desempenho. O DirectX Graphics inclui suporte para gráficos 2D e 3D de alto desempenho.

Para gráficos 3D, use a API do Microsoft Direct3D 11. Mesmo que você tenha um hardware de nível do Microsoft Direct3D 9 ou Microsoft Direct3D 10, você pode usar a API do Direct3D 11 e ter como [destino um](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) dispositivo de nível de recurso 9 \_ x ou de nível de recurso 10 \_ x. Para obter informações sobre como desenvolver gráficos 3D com o DirectX, consulte [criar gráficos 3D com o DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).

para gráficos e texto 2d, use Direct2D e [DirectWrite](./directwrite/direct-write-portal.md) em vez de Windows Graphics Device Interface (GDI).

para compor os bitmaps que o Direct3D 11 ou Direct2D populado, use [DirectComposition](./directcomp/directcomposition-portal.md).

para saber mais sobre como criar um aplicativo da Windows store que usa o directx, confira [criar seu primeiro aplicativo da loja de Windows usando o directx](/previous-versions/windows/apps/br229580(v=win.10)
). Você pode usar o [**Windows. IU:: XAML:: Controls:: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) classe para criar aplicativos DirectX de alto desempenho com uma sobreposição de interface do usuário XAML. para obter mais informações sobre como combinar XAML e DirectX em um aplicativo Windows, consulte [DirectX e interoperabilidade XAML](/previous-versions/windows/apps/hh825871(v=win.10)).

para saber mais sobre como criar um driver de vídeo para Windows 8, consulte [o roteiro para o Windows modelo de driver de vídeo (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).

Se precisar da documentação para versões anteriores do DirectX, consulte [elementos gráficos do DirectX clássico](/windows/desktop/classic-directx-graphics).


 

 
