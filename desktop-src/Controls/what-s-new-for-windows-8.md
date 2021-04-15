---
title: O que há de novo (controles do Windows)
description: Este tópico descreve as diferenças no suporte a temas e estilos visuais entre o Windows 8 e versões anteriores do Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454514"
---
# <a name="whats-new-windows-controls"></a>O que há de novo (controles do Windows)

Este tópico descreve as diferenças no suporte a temas e estilos visuais entre o Windows 8 e versões anteriores do Windows.

## <a name="through-windows-7"></a>Por meio do Windows 7

Com o Windows 7, os estilos visuais estão ativados por padrão, mas o usuário pode desativá-los selecionando o tema clássico do Windows ou desativando o serviço temas. Quando os estilos visuais estão desativados, toda a interface do usuário Obtém a aparência clássica e a maioria das APIs de estilos visuais não estão disponíveis. O modo de estilos visuais foi mantido pelo Windows 7 para dar suporte a vários temas de alto contraste, bem como tema clássico do Windows. Se você quiser dar suporte a estilos visuais e temas de alto contraste no mesmo aplicativo, normalmente precisará manter dois caminhos de código separados para renderizar controles.

## <a name="windows-8-and-later"></a>Windows 8 e posterior

No Windows 8, os estilos visuais não podem ser desativados por meio da página **personalização** das **configurações do PC** ou pela desativação do serviço temas. O modo clássico do Windows não existe mais e o modo de alto contraste foi modificado para funcionar com estilos visuais. Devido a essas alterações, os aplicativos que se destinam apenas ao Windows 8 não precisam mais de dois caminhos de código separados para dar suporte a estilos visuais e temas de alto contraste.

Os estilos visuais no Windows 8 incluem suporte à compatibilidade com versões anteriores para o modo de tema clássico do Windows. Qualquer código de renderização de interface do usuário que funcione em versões anteriores continuará funcionando no Windows 8 sem modificações.

No Windows 8, se você quiser que seu aplicativo dê suporte aos temas de alto contraste baseados em estilos visuais, você precisará incluir o GUID do Windows 8 na seção de compatibilidade do manifesto do aplicativo. Caso contrário, o sistema pressupõe que o aplicativo foi projetado para uma versão anterior e renderiza a área do cliente simulando temas de alto contraste clássicos do Windows. Para obter mais informações, consulte [suporte a temas de alto contraste](supporting-high-contrast-themes.md).

Como nas versões anteriores, o Windows 8 dá suporte à versão 5 e à versão 6 dos controles comuns, com a versão 5 sendo o padrão. Como apenas a versão 6 dá suporte a estilos visuais, você deve especificar a versão 6 no manifesto do aplicativo se desejar que os estilos visuais sejam aplicados aos controles comuns na área do cliente do seu aplicativo. Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).

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

 

 




