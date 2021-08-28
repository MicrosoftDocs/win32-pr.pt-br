---
title: Documento como um instantâneo de propriedades
description: Revise o documento PrintCapabilities como um instantâneo de propriedades. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031334e820b140cb27f7c293741a84e0d8a89c6c9d1c47f89cf83a87a2d3cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033904"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>Documento PrintCapabilities como um instantâneo de propriedades

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O dispositivo descrito pelo PrintCapabilities pode ter propriedades que dependem do estado ou da configuração do dispositivo. Embora o PrintCapabilities represente o espaço de configuração completo de um dispositivo, o provedor PrintCapabilities produz uma instância dependente de configuração do PrintCapabilities chamada documento PrintCapabilities. Este documento PrintCapabilities dependente de configuração evita sobrecarregar o esquema PrintCapabilities com a complexidade de representar dados com vários valores. Mais importante, para aliviar um consumidor do documento PrintCapabilities da carga de extrair o valor apropriado de uma representação de dados de vários valores, todas as instâncias Property e ScoredProperty em um documento PrintCapabilities devem ter valor único. Em outras palavras, cada instância Property e ScoredProperty em um documento PrintCapabilities deve ter um Valor fixo, em relação à configuração de entrada. Cada documento PrintCapabilities pode ser pensado como um instantâneo das propriedades do dispositivo quando o dispositivo está em um estado específico. Consequentemente, antes que um documento PrintCapabilities possa ser construído, a configuração a ser usada deve ser fornecida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



