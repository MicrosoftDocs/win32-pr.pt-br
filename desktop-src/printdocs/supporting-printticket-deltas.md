---
description: Saiba mais sobre como dar suporte a deltas printTicket. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Suporte a deltas PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548774"
---
# <a name="supporting-printticket-deltas"></a>Suporte a deltas PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A Interface do Provedor PrintTicket tem métodos que podem ser usados para fazer alterações incrementais em um PrintTicket existente. As alterações incrementais de PrintTicket podem ser especificadas em um PrintTicket parcial que é conhecido como um delta printTicket. Um PrintTicket revisado é criado mesclando um delta printTicket com um PrintTicket existente. Consulte o próximo documento da Interface do Provedor PrintTicket para obter mais informações sobre métodos que envolvem deltas printTicket.

Quando um delta printTicket é processado, as etapas a seguir devem ser executadas.

1.  Identifique instâncias de Recurso ou ParameterInit que são comuns ao PrintTicket existente (o PrintTicket de destino) e ao delta printTicket.

    -   Para cada Recurso comum ao PrintTicket de destino e ao delta PrintTicket, substitua o Recurso no PrintTicket de destino pelo Recurso correspondente no delta printTicket.

    -   Para cada ParameterInit comum ao PrintTicket de destino e ao delta PrintTicket, substitua ParameterInit no PrintTicket de destino pelo ParameterInit correspondente no delta printTicket.

2.  Copie todas as instâncias restantes de Recurso e ParameterInit no delta PrintTicket para o PrintTicket de destino.

3.  Se o algoritmo de resolução de conflitos permitir que as prioridades sejam especificadas no próprio PrintTicket, você poderá optar por elevar as prioridades das instâncias Feature e ParameterInit nomeadas no delta printTicket.

4.  Execute a validação printTicket, conforme descrito em [PrintTicket Validation Checklist](printticket-validation-checklist.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



