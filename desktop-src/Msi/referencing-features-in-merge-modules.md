---
description: Os módulos de mesclagem operam apenas com componentes e não com recursos. No entanto, algumas tabelas em módulos de mesclagem, como a tabela PublishComponent, contêm campos que se referem aos recursos.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Referenciando recursos em módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2857b71fd651955319457092d9cf689ded954af758e7906b44a761dfa6ad782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375946"
---
# <a name="referencing-features-in-merge-modules"></a>Referenciando recursos em módulos de mesclagem

Os módulos de mesclagem operam apenas com componentes e não com recursos. No entanto, algumas tabelas em módulos de mesclagem, como [a tabela PublishComponent](publishcomponent-table.md), contêm campos que se referem a recursos.

Um GUID nulo: deve ser autor em qualquer campo de um banco de dados de módulo de {00000000-0000-0000-0000-000000000000} mesclagem que faz referência a um recurso. Quando o módulo de mesclagem é mesclado em um pacote de instalação, a ferramenta de mesclagem substitui o GUID nulo pelo recurso especificado no pacote de instalação, exceto para tabelas que exigem tratamento especial, como a tabela [ModuleSignature](modulesignature-table.md) e as tabelas ModuleSequence.

Observe que, se um GUID nulo for usado como uma chave primária, não há garantia de que o valor substituído pela ferramenta de mesclagem seja exclusivo. Os autores de módulos de mesclagem são responsáveis por garantir que nenhuma chave primária existente na interface do usuário seja duplicada quando a ferramenta de mesclagem substituir GUIDs nulos por recursos.

 

 



