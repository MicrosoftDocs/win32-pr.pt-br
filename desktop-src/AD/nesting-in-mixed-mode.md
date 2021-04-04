---
title: Aninhamento em modo misto
description: Este tópico lista as restrições de grupos de segurança em um domínio de modo misto.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Aninhamento no modo misto do AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822260"
---
# <a name="nesting-in-mixed-mode"></a>Aninhamento em modo misto

Este tópico lista as restrições de grupos de segurança em um domínio de modo misto.

Os grupos de segurança em um domínio de modo misto têm as seguintes restrições:

-   Os grupos universais não podem ser criados em domínios de modo misto porque há suporte para o escopo universal somente em domínios de modo nativo do Windows 2000.
-   Um grupo global pode conter contas do mesmo domínio ao qual o grupo pertence. Um grupo global não pode conter grupos universais, qualquer grupo global ou uma conta de outro domínio.
-   Um grupo de domínio local pode conter grupos globais e contas de qualquer domínio ou floresta. Um grupo de domínio local não pode conter nenhum outro grupo local de domínio.

Lembre-se de que os grupos de distribuição podem ser aninhados de acordo com as regras de aninhamento do modo nativo.

 

 




