---
description: Saiba mais sobre a funcionalidade e as informações que o documento de PrintCapabilities não pretende fornecer.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: O que é um documento de PrintCapabilities não
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409889"
---
# <a name="what-a-printcapabilities-document-is-not"></a>O que é um documento de PrintCapabilities não

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Vale a pena listar algumas das funcionalidades e informações que o documento de PrintCapabilities não pretende fornecer.

Um documento de PrintCapabilities:

-   Não representa dados de valores de multivalor (dependentes de configuração).

    Cada documento de PrintCapabilities é construído para uma configuração específica. Nenhuma propriedade ou ScoredProperty no documento pode ter um valor que depende da configuração específica. Na versão do esquema inicial, o provedor de PrintCapabilities deve processar o PrintTicket de entrada e criar um documento de PrintCapabilities que contenha valores de propriedade apropriados para a configuração especificada no PrintTicket.

-   Não contém informações de restrição.

    O documento PrintCapabilities não indica quais configurações são permitidas e quais não são permitidas. Na versão do esquema inicial, o provedor de PrintCapabilities deve armazenar todas as informações necessárias para validar as configurações, fornecer um método que valida o PrintTicket de entrada e retornar um PrintTicket corrigido caso o PrintTicket especificado viole uma ou mais restrições.

-   Não contém informações dinâmicas do dispositivo.

    Há muita sobrecarga envolvida na construção do documento PrintCapabilities para que ele seja usado para manter a alteração rápida de informações de status, como níveis de tinta, papel restante em cada bandeja ou status de emperramento de papel.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



