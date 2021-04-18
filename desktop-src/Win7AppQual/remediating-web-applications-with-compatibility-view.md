---
description: .
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43f4ff54a919058127a5f72ba60f3683c6583e1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105785163"
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



 

 

 



