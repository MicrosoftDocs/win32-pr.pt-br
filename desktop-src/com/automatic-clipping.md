---
title: Recorte automático
description: Recorte automático
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292507"
---
# <a name="automatic-clipping"></a>Recorte automático

É altamente recomendável que um contêiner de controle ActiveX dê suporte ao recorte automático de seus controles. Isso resultará em uma operação mais eficiente para a maioria dos controles. Se o recorte automático tiver suporte, a propriedade de ambiente autoclip deve ter suporte e ter um valor de **true**.

O recorte automático é a capacidade de um contêiner de garantir que a saída desenhada de um controle vá apenas para a região de recorte atual do contêiner. Em um contêiner que dá suporte a recorte automático, um controle pode pintar sem considerar sua região de recorte, porque o contêiner cortará automaticamente qualquer pintura que ocorra fora da área do controle. Se um contêiner não oferecer suporte a recorte automático, os controles gerados pelo CDK criarão uma janela pai extra se uma região de recorte não nula for passada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

 




