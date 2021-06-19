---
description: Esta visão geral da funcionalidade PrintTicket descreve o formato para expressar informações de configuração do dispositivo e o uso de um PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Visão geral da funcionalidade PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408539"
---
# <a name="overview-of-printticket-functionality"></a>Visão geral da funcionalidade PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O PrintTicket utiliza um formato baseado em XML para expressar informações de configuração do dispositivo usando os constructos de recurso/opção e parâmetro da Estrutura de Esquema de Impressão. Isso inclui todos os tipos de elementos padrão, bem como os recursos de extensibilidade da Estrutura de Esquema de Impressão. Um PrintTicket é assumido como uma descrição independente de como uma única página deve ser processada. As etapas envolvidas na extração e na construção desse printTicket de um formato de documento específico não são abordadas aqui.

Um PrintTicket pode ser usado para obter um documento PrintCapabilities que descreve as características do dispositivo para uma configuração específica. Como alternativa, o PrintTicket pode ser enviado com um conjunto de instruções de renderização para produzir uma página de saída renderizada e processada de acordo com a configuração especificada no PrintTicket.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



