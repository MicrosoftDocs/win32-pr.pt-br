---
title: Novidades (controles Windows)
description: Este tópico descreve as diferenças no suporte para temas e estilos visuais entre Windows 8 e versões anteriores do Windows .
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
# <a name="whats-new-windows-controls"></a>Novidades (controles Windows)

Este tópico descreve as diferenças no suporte para temas e estilos visuais entre Windows 8 e versões anteriores do Windows .

## <a name="through-windows-7"></a>Até Windows 7

Por Windows 7, os estilos visuais estão ativos por padrão, mas o usuário pode acioná-los selecionando Windows Tema Clássico ou desligando o serviço Temas. Quando os estilos visuais estão desligados, todas as interfaces do usuário têm a aparência clássica e a maioria das APIs de estilos visuais não estão disponíveis. Os estilos visuais fora do modo foram retidos por meio Windows 7 para dar suporte aos vários temas de alto contraste, bem como Windows tema Clássico. Se você quiser dar suporte a estilos visuais e temas de alto contraste no mesmo aplicativo, normalmente precisará manter dois caminhos de código separados para renderizar controles.

## <a name="windows-8-and-later"></a>Windows 8 e posterior

No Windows 8, os estilos visuais não podem  ser desligados por meio da página Personalização do computador Configurações ou desligando o serviço Temas.  Windows O modo clássico não existe mais e o modo de alto contraste foi modificado para funcionar com estilos visuais. Devido a essas alterações, os aplicativos destinados somente Windows 8 precisam de dois caminhos de código separados para dar suporte a estilos visuais e temas de alto contraste.

Os estilos visuais no Windows 8 incluem suporte à compatibilidade com Windows modo de temas clássico. Qualquer código de renderização de interface do usuário que funcione em versões anteriores continuará funcionando em Windows 8 sem modificações.

No Windows 8, se você quiser que seu aplicativo seja compatível com os temas de alto contraste baseados em estilos visuais, será necessário incluir o GUID do Windows 8 na seção de compatibilidade do manifesto do aplicativo. Caso contrário, o sistema pressupõe que o aplicativo foi projetado para uma versão anterior e renderiza a área do cliente simulando Windows temas clássicos de alto contraste. Para obter mais informações, consulte [Support Alto Contraste Themes](supporting-high-contrast-themes.md).

Assim como nas versões anteriores, Windows 8 dá suporte à versão 5 e à versão 6 dos controles comuns, com a versão 5 sendo o padrão. Como apenas a versão 6 dá suporte a estilos visuais, você deve especificar a versão 6 no manifesto do aplicativo se quiser que os estilos visuais sejam aplicados aos controles comuns na área de cliente do aplicativo. Para obter mais informações, consulte [Habilitando estilos visuais.](cookbook-overview.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitar estilos visuais](cookbook-overview.md)
</dt> <dt>

[Temas Alto Contraste suporte](supporting-high-contrast-themes.md)
</dt> <dt>

[Estilos visuais](themes-overview.md)
</dt> <dt>

[Visão geral dos estilos visuais](visual-styles-overview.md)
</dt> </dl>

 

 




