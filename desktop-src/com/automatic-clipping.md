---
title: Recorte automático
description: Recorte automático
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dabc3fd7ece50250ee9e1fea89ff23dd23db533dfcc90d5a939ce1b563ce764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551232"
---
# <a name="automatic-clipping"></a>Recorte automático

É altamente recomendável que um contêiner de controle ActiveX suporte ao recorte automático de seus controles. Isso resultará em uma operação mais eficiente para a maioria dos controles. Se há suporte para recorte automático, a propriedade ambiente AutoClip deve ter suporte e ter um valor **true.**

O recorte automático é a capacidade de um contêiner de garantir que a saída desenhada de um controle vá apenas para a região de recorte atual do contêiner. Em um contêiner que dá suporte a recorte automático, um controle pode pintar sem considerar sua região de recorte, pois o contêiner cortará automaticamente qualquer pintura que ocorre fora da área do controle. Se um contêiner não dá suporte a recorte automático, os controles gerados pela CDK criarão uma janela pai extra se uma região de recorte não nula for passada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

 




