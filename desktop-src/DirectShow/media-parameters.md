---
description: Parâmetros de mídia
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Parâmetros de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837616"
---
# <a name="media-parameters"></a>Parâmetros de mídia

Os parâmetros de mídia permitem que um aplicativo configure as propriedades de um objeto de forma que elas sejam alteradas com o passar do tempo de forma matematicamente determinística.

Por exemplo, suponha que um engenheiro de som esteja misturando uma fita mestre digital e queira aplicar um pequeno atraso a uma seção vocal para preencher o som. O efeito será dissonante se o atraso for recortado abruptamente. Em vez disso, o efeito deve começar de 100% seco (sem atraso) e a mistura úmida/seca deve aumentar gradualmente até atingir o nível desejado. Além disso, essa transição deve seguir uma curva suave ou uma progressão linear. Para dar suporte a esse cenário, um DMO pode expor as seguintes interfaces:

-   [**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contém métodos para descobrir informações sobre as propriedades com suporte. Normalmente, o cliente chamará esses métodos antes de começar a transmitir dados.
-   [**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contêm métodos para definir as curvas que um parâmetro seguirá durante o streaming.

Essas interfaces são projetadas principalmente para DMOs, mas qualquer objeto pode dar suporte a elas. Nesta seção, o *parâmetro* Term refere-se a qualquer propriedade que ofereça suporte a essas duas interfaces.

Esta seção contém os seguintes tópicos:

-   [Curvas de parâmetro](parameter-curves.md)
-   [Informações de parâmetro](parameter-information.md)
-   [Segmentos de envelope](envelope-segments.md)
-   [Calculando valores de parâmetro](calculating-parameter-values.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de mídia do DirectX](directx-media-objects.md)
</dt> </dl>

 

 



