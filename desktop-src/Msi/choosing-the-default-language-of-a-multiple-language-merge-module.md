---
description: O idioma padrão para um módulo de mesclagem é o idioma listado na Tabela ModuleSignature do módulo antes que as transformaçãos de idioma sejam aplicadas. Esse também é o primeiro idioma listado na propriedade Resumo do Modelo.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Escolhendo o idioma padrão de um módulo de mesclagem de vários idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c174a3917538b1562626819f8ba2bf07864c9169c27e717a078cca8d64992ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145652"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>Escolhendo o idioma padrão de um módulo de mesclagem de vários idiomas

O idioma padrão para um módulo de mesclagem é o idioma listado na Tabela [ModuleSignature](modulesignature-table.md) do módulo antes que as transformaçãos de idioma sejam aplicadas. Esse também é o primeiro idioma listado na propriedade [**Resumo do**](template-summary.md) Modelo.

O idioma padrão do módulo deve ser um dos idiomas mais específicos que você suporta, pois o idioma padrão sempre é verificado primeiro e, se ele satisfaz o idioma solicitado, ele é usado mesmo se outro idioma for uma melhor combinação. Por exemplo, se um módulo dá suporte a 1033 e 0, 1033 deve ser o idioma padrão. Se 0 fosse o idioma padrão, ele sempre atenderia a qualquer solicitação e a transformação 1033 nunca seria usada, mesmo se 1033 fosse o idioma exato solicitado.

 

 



