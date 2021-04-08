---
title: Aninhamento no modo nativo
description: A lista a seguir descreve o que pode estar contido em um grupo que existe em um domínio de modo nativo.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Aninhamento no AD no modo nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822259"
---
# <a name="nesting-in-native-mode"></a>Aninhamento no modo nativo

A lista a seguir descreve o que pode estar contido em um grupo que existe em um domínio de modo nativo. Essa mesma lista também se aplica a grupos de distribuição em domínios de modo misto. O escopo do grupo determina essas regras de confinamento.

-   Um grupo universal pode conter outros grupos universais, grupos globais e contas de qualquer domínio dentro da floresta em que esse grupo universal reside.
-   Um grupo global pode conter outros grupos globais e contas do mesmo domínio ao qual o grupo pertence. Um grupo global não pode conter grupos universais ou qualquer conta ou grupo global de outro domínio.
-   Um grupo de domínio local pode conter grupos universais, grupos globais e contas de qualquer domínio ou floresta. Um grupo de domínio local também pode conter outros grupos locais de domínio do mesmo domínio ao qual o grupo pertence. Um grupo de domínio local não pode conter outros grupos locais de domínio de qualquer outro domínio ou floresta.

 

 




