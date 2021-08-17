---
title: o que há de novo (controles de Windows)
description: este tópico descreve as diferenças no suporte a temas e estilos visuais entre Windows 8 e versões anteriores do Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7801eea011aabb05663cc2e29f18e0dd58edc9fddc4f32014fcffb96c559cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957545"
---
# <a name="whats-new-windows-controls"></a>o que há de novo (controles de Windows)

este tópico descreve as diferenças no suporte a temas e estilos visuais entre Windows 8 e versões anteriores do Windows.

## <a name="through-windows-7"></a>até Windows 7

até Windows 7, os estilos visuais são ativados por padrão, mas o usuário pode desativá-los selecionando Windows tema clássico ou desativando o serviço temas. Quando os estilos visuais estão desativados, toda a interface do usuário Obtém a aparência clássica e a maioria das APIs de estilos visuais não estão disponíveis. o modo de estilos visuais foi mantido por meio do Windows 7 para dar suporte a vários temas de alto contraste, bem como Windows tema clássico. Se você quiser dar suporte a estilos visuais e temas de alto contraste no mesmo aplicativo, normalmente precisará manter dois caminhos de código separados para renderizar controles.

## <a name="windows-8-and-later"></a>Windows 8 e posterior

no Windows 8, os estilos visuais não podem ser desativados por meio da página **personalização** do **PC Configurações** ou desativando o serviço temas. Windows O modo clássico não existe mais e o modo de alto contraste foi modificado para funcionar com estilos visuais. devido a essas alterações, os aplicativos que se destinam apenas a Windows 8 não precisam mais de dois caminhos de código separados para dar suporte a estilos visuais e temas de alto contraste.

os estilos visuais no Windows 8 incluem suporte à compatibilidade com versões anteriores para Windows modo clássico de temas. qualquer código de renderização de interface do usuário que funcione em versões anteriores continuará a funcionar em Windows 8 sem modificações.

em Windows 8, se você quiser que seu aplicativo dê suporte aos temas de alto contraste baseados em estilos visuais, você precisará incluir o GUID Windows 8 na seção de compatibilidade do manifesto do aplicativo. caso contrário, o sistema pressupõe que o aplicativo foi projetado para uma versão anterior e renderiza a área do cliente simulando Windows temas de alto contraste clássicos. Para obter mais informações, consulte [suporte a temas de alto contraste](supporting-high-contrast-themes.md).

como nas versões anteriores, Windows 8 dá suporte à versão 5 e à versão 6 dos controles comuns, com a versão 5 sendo o padrão. Como apenas a versão 6 dá suporte a estilos visuais, você deve especificar a versão 6 no manifesto do aplicativo se desejar que os estilos visuais sejam aplicados aos controles comuns na área do cliente do seu aplicativo. Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitar estilos visuais](cookbook-overview.md)
</dt> <dt>

[Suporte a temas de Alto Contraste](supporting-high-contrast-themes.md)
</dt> <dt>

[Estilos visuais](themes-overview.md)
</dt> <dt>

[Visão geral dos estilos visuais](visual-styles-overview.md)
</dt> </dl>

 

 




