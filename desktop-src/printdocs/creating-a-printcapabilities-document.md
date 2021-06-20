---
description: Depois que um PrintTicket é validado, ele pode ser usado para criar um instantâneo de PrintCapabilities.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Criando um documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96ea51cef9dfd0f351704b3b71a7f6163737736
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409509"
---
# <a name="creating-a-printcapabilities-document"></a>Criando um documento PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Depois que um PrintTicket é validado, ele pode ser usado para criar um instantâneo de PrintCapabilities. O provedor deve ter uma representação interna para qualquer Propriedade cujo Valor depende da configuração do dispositivo. Por exemplo, se SpotDiameter for uma Propriedade que depende dos recursos Resolution e MediaType, uma representação interna do SpotDiameter relacionada aos vários valores de Resolution e MediaType poderá aparecer como na tabela a seguir:



| Resolução      | MediaType         | SpotDiameter   |
|-----------------|-------------------|----------------|
| 300<br/>  | Bond<br/>   | 520<br/> |
| 300<br/>  | Brilhante<br/> | 350<br/> |
| 600<br/>  | Bond<br/>   | 330<br/> |
| 600<br/>  | Brilhante<br/> | 180<br/> |
| 1200<br/> | Bond<br/>   | 250<br/> |
| 1200<br/> | Brilhante<br/> | 100<br/> |



 

Para este exemplo, o provedor PrintCapabilities deve usar o PrintTicket fornecido para selecionar a entrada adequada na tabela interna e relatar isso como o Valor para a propriedade SpotDiameter. Esse processo é repetido para cada Propriedade com valores múltiplos (para cada Propriedade cujo Valor depende da configuração). A [seção Esquema de PrintCapabilities e](printcapabilities-schema-and-document-construction.md) Construção de Documentos descreve as outras etapas envolvidas na criação de um instantâneo do PrintCapabilities.

Para criar um instantâneo do documento PrintCapabilities padrão, forneça um PrintTicket padrão (em vez de um PrintTicket arbitrário) para o método que cria documentos PrintCapabilities.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




