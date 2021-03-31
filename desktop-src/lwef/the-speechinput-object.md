---
title: O objeto SpeechInput
description: O objeto SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916426"
---
# <a name="the-speechinput-object"></a>O objeto SpeechInput

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O objeto [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) fornece acesso às propriedades de entrada de fala mantidas pelo servidor do agente. As propriedades são somente leitura para aplicativos cliente, mas o usuário pode alterá-las na folha de propriedades do Microsoft Agent. O servidor retornará valores somente se um mecanismo de fala compatível tiver sido instalado e estiver habilitado.

As propriedades [**Engine**](https://www.bing.com/search?q=**Engine**), [**installed**](https://www.bing.com/search?q=**Installed**)e [**Language**](https://www.bing.com/search?q=**Language**) não têm mais suporte, mas (para compatibilidade com versões anteriores) retornarão valores nulos se consultados. Para consultar ou definir o modo de reconhecimento de fala, use a propriedade [**SRModeID**](srmodeid-property.md) .

-   [Propriedades de SpeechInput](speechinput-properties.md)

 

 




