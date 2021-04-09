---
description: Alguns objetos dão suporte a apenas um identificador de cada vez.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Limitações de identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171471"
---
# <a name="handle-limitations"></a>Limitações de identificador

Alguns objetos dão suporte a apenas um identificador de cada vez. O sistema fornece o identificador quando um aplicativo cria o objeto e invalida o identificador quando o aplicativo destrói o objeto. Outros objetos dão suporte a vários identificadores para um único objeto. O sistema operacional remove automaticamente o objeto da memória depois que o último identificador para o objeto é fechado.

O número total de identificadores abertos no sistema é limitado apenas pela quantidade de memória disponível. Alguns tipos de objeto dão suporte a um número limitado de identificadores por sessão ou por processo.

 

 



