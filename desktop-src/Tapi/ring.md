---
description: Um único telefone pode ser capaz de tocar com diferentes modos de toque.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Anel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921692"
---
# <a name="ring"></a>Anel

Um único telefone pode ser capaz de tocar com diferentes modos de toque. Considerando a ampla variedade de modos de toque disponíveis, os modos de toque são identificados por meio de seu número de modo de toque. Um número de modo de anel varia de zero para o número de modos de anel disponíveis menos um.

As funções que um aplicativo usaria para controlar os modos de toque de um dispositivo de telefone são [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), que toca um dispositivo de telefone aberto de acordo com um determinado modo de toque e [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), que retorna o modo de toque atual de um dispositivo de telefone aberto.

Quando o modo de anel de um dispositivo de telefone é alterado, uma mensagem de [**\_ estado de telefone**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado. Os parâmetros dessa mensagem fornecem uma indicação da alteração.

 

 



