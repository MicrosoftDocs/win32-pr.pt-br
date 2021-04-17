---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Suporte a deltas do PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105765784"
---
# <a name="supporting-printticket-deltas"></a>Suporte a deltas do PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A interface do provedor PrintTicket tem métodos que podem ser usados para fazer alterações incrementais em um PrintTicket existente. As alterações incrementais do PrintTicket podem ser especificadas em um PrintTicket parcial conhecido como um Delta PrintTicket. Um PrintTicket revisado é criado pela mesclagem de um Delta PrintTicket com um PrintTicket existente. Consulte o documento da interface do provedor do PrintTicket em breve para obter mais informações sobre métodos envolvendo deltas PrintTicket.

Quando um Delta PrintTicket é processado, as etapas a seguir devem ser executadas.

1.  Identifique as instâncias de recurso ou ParameterInit que são comuns ao PrintTicket existente (o PrintTicket de destino) e ao Delta do PrintTicket.

    -   Para cada recurso comum ao PrintTicket de destino e ao Delta do PrintTicket, substitua o recurso no PrintTicket de destino pelo recurso correspondente no Delta do PrintTicket.

    -   Para cada ParameterInit comum ao PrintTicket de destino e ao Delta do PrintTicket, substitua o ParameterInit no PrintTicket de destino pelo ParameterInit correspondente no Delta do PrintTicket.

2.  Copie todas as instâncias restantes do recurso e do ParameterInit no Delta do PrintTicket para o PrintTicket de destino.

3.  Se o algoritmo de resolução de conflitos permitir que as prioridades sejam especificadas no próprio PrintTicket, você poderá optar por elevar as prioridades do recurso e das instâncias ParameterInit nomeadas no Delta do PrintTicket.

4.  Execute a validação de PrintTicket conforme descrito na [lista de verificação de validação do PrintTicket](printticket-validation-checklist.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



