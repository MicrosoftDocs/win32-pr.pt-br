---
description: Um único telefone pode ser capaz de tocar com diferentes modos de anel.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Anel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d183c217447ca02bf5ee0c535360eecaea1f3c209cdb813ad58b77268f234d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773356"
---
# <a name="ring"></a>Anel

Um único telefone pode ser capaz de tocar com diferentes modos de anel. Dada a ampla variedade de modos de anel disponíveis, os modos de anel são identificados por meio de seu número de modo de anel. Um número de modo de anel varia de zero ao número de modos de anel disponíveis menos um.

As funções que um aplicativo usaria para controlar os modos de anel de um dispositivo de telefone são [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), que anéis um dispositivo de telefone aberto de acordo com um determinado modo de anel, e [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), que retorna o modo de anel atual de um dispositivo de telefone aberto.

Quando o modo de anel de um dispositivo de telefone é alterado, uma mensagem [**PHONE \_ STATE**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado. Os parâmetros para essa mensagem fornecem uma indicação da alteração.

 

 



