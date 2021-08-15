---
title: O objeto SpeechInput
description: O objeto SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d96dd52d5847b3fbaa81bbc21d4015698655fba1fe2523aaddc065e6d2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975516"
---
# <a name="the-speechinput-object"></a>O objeto SpeechInput

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O [**objeto SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) fornece acesso às propriedades de entrada de fala mantidas pelo servidor do Agent. As propriedades são somente leitura para aplicativos cliente, mas o usuário pode alterá-las na folha de propriedades do Microsoft Agent. O servidor retornará valores somente se um mecanismo de fala compatível tiver sido instalado e estiver habilitado.

As [**propriedades Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**)e [**Language**](https://www.bing.com/search?q=**Language**) não têm mais suporte, mas (para compatibilidade com backward) retornam valores nulos se consultados. Para consultar ou definir o modo de um reconhecimento de fala, use a [**propriedade SRModeID.**](srmodeid-property.md)

-   [Propriedades speechInput](speechinput-properties.md)

 

 




