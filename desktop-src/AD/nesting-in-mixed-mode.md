---
title: Aninhamento no modo misto
description: Este tópico lista as restrições de grupos de segurança em um domínio de modo misto.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Aninhamento no AD de Modo Misto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c53fd79cb10c452dbb363c3d6803071e6e52871f0ce87b03f9d06a61eaece8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185818"
---
# <a name="nesting-in-mixed-mode"></a>Aninhamento no modo misto

Este tópico lista as restrições de grupos de segurança em um domínio de modo misto.

Os grupos de segurança em um domínio de modo misto têm as seguintes restrições:

-   Grupos universais não podem ser criados em domínios de modo misto porque o escopo universal tem suporte apenas Windows domínios de modo nativo 2000.
-   Um grupo global pode conter contas do mesmo domínio ao qual o grupo pertence. Um grupo global não pode conter nenhum grupo universal, nenhum grupo global ou uma conta de outro domínio.
-   Um grupo local de domínio pode conter grupos globais e contas de qualquer domínio ou floresta. Um grupo local de domínio não pode conter nenhum outro grupo local de domínio.

Esteja ciente de que os grupos de distribuição podem ser aninhados de acordo com as regras de aninhamento para o modo nativo.

 

 




