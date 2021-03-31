---
description: Em sistemas operacionais de 64 bits, Windows Installer pode chamar ações personalizadas que foram compiladas para sistemas de 32 bits ou de 64 bits.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: Ações personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662075"
---
# <a name="64-bit-custom-actions"></a>Ações personalizadas de 64 bits

Em sistemas operacionais de 64 bits, Windows Installer pode chamar ações personalizadas que foram compiladas para sistemas de 32 bits ou de 64 bits.

Uma ação personalizada de 64 bits baseada em [scripts](scripts.md) deve ser explicitamente marcada como uma ação personalizada de 64 bits, adicionando o bit **msidbCustomActionType64BitScript** ao tipo numérico Actions personalizado na coluna Type da [tabela CustomAction](customaction-table.md).



| Constante                             | Hexadecimal | Decimal | Significado                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| **msidbCustomActionType64BitScript** | 0x0001000   | 4096    | Esta é uma ação personalizada de 64 bits escrita em [scripts](scripts.md). |



 

Ações personalizadas com base em [arquivos executáveis](executable-files.md) ou [bibliotecas de vínculo dinâmico](dynamic-link-libraries.md) que foram compatíveis com sistemas operacionais de 64 bits não exigem a inclusão desse bit adicional na coluna Type da tabela CustomAction.

 

 



