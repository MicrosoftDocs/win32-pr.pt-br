---
title: Aninhamento no modo nativo
description: A lista a seguir descreve o que pode estar contido em um grupo que existe em um domínio de modo nativo.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Aninhamento no AD do modo nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3fa2842981354738cd4ef112ef278fa33ca310adeedcd62fb245a2663cce07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025734"
---
# <a name="nesting-in-native-mode"></a>Aninhamento no modo nativo

A lista a seguir descreve o que pode estar contido em um grupo que existe em um domínio de modo nativo. Essa mesma lista também se aplica a grupos de distribuição em domínios de modo misto. O escopo do grupo determina essas regras de contenção.

-   Um grupo universal pode conter outros grupos universais, grupos globais e contas de qualquer domínio dentro da floresta em que reside esse Grupo Universal.
-   Um grupo global pode conter outros grupos globais e contas do mesmo domínio ao que o grupo pertence. Um grupo global não pode conter nenhum grupo universal ou qualquer grupo global ou conta de outro domínio.
-   Um grupo local de domínio pode conter grupos universais, grupos globais e contas de qualquer domínio ou floresta. Um grupo local de domínio também pode conter outros grupos locais de domínio do mesmo domínio ao que o grupo pertence. Um grupo local de domínio não pode conter outros grupos locais de domínio de qualquer outro domínio ou floresta.

 

 




