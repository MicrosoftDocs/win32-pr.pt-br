---
description: Em sistemas operacionais de 64 bits, Windows instalador pode chamar ações personalizadas compiladas para sistemas de 32 ou 64 bits.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Usando ações personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d94e5d6118c0f2f5dcf5a297718e135cce25a69bea0f48a2d4ea5df4cc0463
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809106"
---
# <a name="using-64-bit-custom-actions"></a>Usando ações personalizadas de 64 bits

Em sistemas operacionais de 64 bits, Windows instalador pode chamar ações personalizadas compiladas para sistemas de 32 ou 64 bits. Uma ação personalizada de 64 bits baseada em [Scripts](scripts.md) deve ser marcada explicitamente como uma ação personalizada de 64 bits adicionando o bit **msidbCustomActionType64BitScript** ao tipo numérico de ação personalizada na coluna Tipo da Tabela [CustomAction](customaction-table.md). Ações personalizadas baseadas em arquivos [executáveis](executable-files.md) ou bibliotecas de [vínculo](dynamic-link-libraries.md) dinâmico que são cumpridas para sistemas operacionais de 64 bits não exigem a inclusão desse bit adicional na coluna Tipo da Tabela CustomAction.

Para obter mais informações, consulte Ações personalizadas de [64 bits.](64-bit-custom-actions.md)

 

 



