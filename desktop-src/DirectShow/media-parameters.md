---
description: Parâmetros de mídia
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Parâmetros de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37cf7229cac3deb5b31a6c6879fd3b5896e5f4098a4cce64ac42d19970f5c569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584336"
---
# <a name="media-parameters"></a>Parâmetros de mídia

Os parâmetros de mídia permitem que um aplicativo configure as propriedades de um objeto para que elas mudem ao longo do tempo de maneira matematicamente determinística.

Por exemplo, suponha que um engenheiro de som está combinando uma fita mestra digital e deseja aplicar um pequeno atraso a uma seção vocal para preencher o som. O efeito será jarring se o atraso for interrompida de forma repentina. Em vez disso, o efeito deve começar 100% de seta (sem atraso) e a combinação de umidade/umidade deve aumentar gradualmente até atingir o nível desejado. Além disso, essa transição deve seguir uma curva suave ou progressão linear. Para dar suporte a esse cenário, DMO pode expor as seguintes interfaces:

-   [**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contém métodos para descobrir informações sobre as propriedades com suporte. Normalmente, o cliente chamará esses métodos antes de começar a transmitir dados.
-   [**IMediaParams contêm**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) métodos para definir as curvas que um parâmetro seguirá durante o streaming.

Essas interfaces são projetadas principalmente para DMOs, mas qualquer objeto pode dar suporte a elas. Nesta seção, o termo *parâmetro refere-se* a qualquer propriedade que dá suporte a essas duas interfaces.

Esta seção contém os seguintes tópicos:

-   [Curvas de parâmetro](parameter-curves.md)
-   [Informações de parâmetro](parameter-information.md)
-   [Segmentos de envelope](envelope-segments.md)
-   [Calculando valores de parâmetro](calculating-parameter-values.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de mídia do DirectX](directx-media-objects.md)
</dt> </dl>

 

 



