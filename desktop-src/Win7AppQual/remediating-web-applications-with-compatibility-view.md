---
description: Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116354"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade

Esta seção descreve as etapas básicas de mitigação e como planejar a compatibilidade de aplicativos futuramente enquanto você está abordando quaisquer problemas agora.

O Windows Internet Explorer dá suporte aos modelos herdados do Internet Explorer sempre que possível para que os sites que você desenvolve para eles continuem a se comportarem conforme o esperado nas versões mais recentes do Internet Explorer. A partir do Windows Internet Explorer 8, você pode optar por oferecer suporte a comportamentos herdados selecionando o modo de renderização página por página.

O Internet Explorer 8 inclui os seguintes modos de renderização que podem ser definidos usando o cabeçalho X-UA-Compatible.



| Valor do conteúdo | Descrição                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Use o modo peculiaridades.                                                                      |
| IE = 7          | Sempre use o modo do Windows Internet Explorer 7.                                          |
| IE=EmulateIE7 | Exibir no modo do Internet Explorer 7, a menos que o site tenha o DOCTYPE de inpeculiars.           |
| IE = 8          | Sempre use o modo do Internet Explorer 8.                                                  |
| IE=EmulateIE8 | Substitua a exibição de compatibilidade em computadores cliente e use o modo do Internet Explorer 8.      |
| IE=Edge       | Exibir no modo mais recente. No Internet Explorer 8, esse valor é equivalente ao IE = 8. |



 

Os tópicos a seguir descrevem como atualizar aplicativos Web usando o modo de exibição de compatibilidade.



| Tópico                                                                                                  | Descrição                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [O que é o modo de exibição de compatibilidade](what-is-compatibility-view-.md)                                          | Descreve o modo de exibição de compatibilidade.                                                  |
| [Por que você precisa do modo de exibição de compatibilidade?](why-do-you-need-compatibility-view-.md)                         | Descreve por que você deve usar o modo de exibição de compatibilidade.                               |
| [Use a marca meta para garantir a compatibilidade futura](use-the-meta-tag-to-ensure-future-compatibility.md) | Descreve como você pode usar o elemento **meta** para garantir a compatibilidade futura. |



 

 

 



