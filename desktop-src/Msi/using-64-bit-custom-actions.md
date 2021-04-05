---
description: Em sistemas operacionais de 64 bits, Windows Installer pode chamar ações personalizadas que são compiladas para sistemas de 32 bits ou de 64 bits.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Usando ações personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922128"
---
# <a name="using-64-bit-custom-actions"></a>Usando ações personalizadas de 64 bits

Em sistemas operacionais de 64 bits, Windows Installer pode chamar ações personalizadas que são compiladas para sistemas de 32 bits ou de 64 bits. Uma ação personalizada de 64 bits baseada em [scripts](scripts.md) deve ser explicitamente marcada como uma ação personalizada de 64 bits, adicionando o bit **msidbCustomActionType64BitScript** ao tipo numérico de ação personalizada na coluna tipo da [tabela CustomAction](customaction-table.md). Ações personalizadas com base em [arquivos executáveis](executable-files.md) ou [bibliotecas de vínculo dinâmico](dynamic-link-libraries.md) que são compatíveis com sistemas operacionais de 64 bits não exigem a inclusão desse bit adicional na coluna Type da tabela CustomAction.

Para obter mais informações, consulte [ações personalizadas de 64 bits](64-bit-custom-actions.md).

 

 



