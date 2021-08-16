---
description: Corrigindo problemas de compatibilidade em aplicativos Web usando Modo de Exibição de Compatibilidade
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Corrigindo problemas de compatibilidade em aplicativos Web usando Modo de Exibição de Compatibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dd876dcf8d25ebe7e6cca15ea88bfeba52aa29e3e5d83680815c15f8bda46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329505"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Corrigindo problemas de compatibilidade em aplicativos Web usando Modo de Exibição de Compatibilidade

Esta seção descreve as etapas básicas de mitigação e como planejar a compatibilidade futura do aplicativo enquanto você está tratando quaisquer problemas agora.

Windows Internet Explorer dá suporte aos modelos de Internet Explorer herdados sempre que possível para que os sites que você desenvolve para eles continuem se comportando conforme o esperado em versões mais recentes do Internet Explorer. Começando com Windows Internet Explorer 8, você pode optar por dar suporte a comportamentos herdados selecionando o modo de renderização página a página.

Internet Explorer 8 inclui os seguintes modos de renderização que você pode definir usando o header Compatível com X-UA.



| Valor do conteúdo | Descrição                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Use o modo de características.                                                                      |
| IE=7          | Sempre use Windows Internet Explorer modo 7.                                          |
| IE=EmulateIE7 | Exibir no Internet Explorer 7, a menos que o site tenha as características DOCTYPE.           |
| IE=8          | Sempre use Internet Explorer modo 8.                                                  |
| IE=EmulateIE8 | Substitua Modo de Exibição de Compatibilidade em máquinas cliente e use Internet Explorer modo 8.      |
| IE=Edge       | Exibir no modo mais recente. No Internet Explorer 8, esse valor é equivalente a IE=8. |



 

Os tópicos a seguir descrevem como atualizar aplicativos Web usando Modo de Exibição de Compatibilidade.



| Tópico                                                                                                  | Descrição                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [O que é Modo de Exibição de Compatibilidade](what-is-compatibility-view-.md)                                          | Descreve Modo de Exibição de Compatibilidade.                                                  |
| [Por que você precisa Modo de Exibição de Compatibilidade?](why-do-you-need-compatibility-view-.md)                         | Descreve por que você deve usar Modo de Exibição de Compatibilidade.                               |
| [Usar a meta tag para garantir a compatibilidade futura](use-the-meta-tag-to-ensure-future-compatibility.md) | Descreve como você pode usar o **meta elemento** para garantir a compatibilidade futura. |



 

 

 



