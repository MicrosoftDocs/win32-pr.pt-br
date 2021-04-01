---
description: Os módulos de mesclagem só funcionam com componentes e não com recursos. No entanto, algumas tabelas em módulos de mesclagem, como a tabela PublishComponent, contêm campos que se referem a recursos.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Referenciando recursos em módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921639"
---
# <a name="referencing-features-in-merge-modules"></a>Referenciando recursos em módulos de mesclagem

Os módulos de mesclagem só funcionam com componentes e não com recursos. No entanto, algumas tabelas em módulos de mesclagem, como a [tabela PublishComponent](publishcomponent-table.md), contêm campos que se referem a recursos.

Um GUID nulo: {00000000-0000-0000-0000-000000000000} deve ser criado em qualquer campo de um banco de dados de módulo de mesclagem que faça referência a um recurso. Quando o módulo de mesclagem é mesclado em um pacote de instalação, a ferramenta de mesclagem substitui o GUID nulo pelo recurso especificado no pacote de instalação, exceto para tabelas que exigem tratamento especial, como a [tabela ModuleSignature](modulesignature-table.md) e as tabelas ModuleSequence.

Observe que, se um GUID NULL for usado como uma chave primária, não haverá garantia de que o valor substituído pela ferramenta de mesclagem seja exclusivo. Os autores de módulos de mesclagem são responsáveis por garantir que nenhuma chave primária existente na interface do usuário seja duplicada quando a ferramenta de mesclagem substituir os GUIDs nulos por recursos.

 

 



