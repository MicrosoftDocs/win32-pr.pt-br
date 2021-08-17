---
description: Alguns objetos dão suporte a apenas um identificador de cada vez.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Limitações de identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f194ed8464d2731c15e9b88ae62549f9fa090928c14cf7dc66e139944863b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764404"
---
# <a name="handle-limitations"></a>Limitações de identificador

Alguns objetos dão suporte a apenas um identificador de cada vez. O sistema fornece o identificador quando um aplicativo cria o objeto e invalida o identificador quando o aplicativo destrói o objeto. Outros objetos dão suporte a vários identificadores para um único objeto. O sistema operacional remove automaticamente o objeto da memória depois que o último identificador para o objeto é fechado.

O número total de identificadores abertos no sistema é limitado apenas pela quantidade de memória disponível. Alguns tipos de objeto dão suporte a um número limitado de identificadores por sessão ou por processo.

 

 



