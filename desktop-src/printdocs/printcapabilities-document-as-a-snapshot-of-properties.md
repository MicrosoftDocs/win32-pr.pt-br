---
title: Documento como um instantâneo das propriedades
description: Examine o documento PrintCapabilities como um instantâneo das propriedades. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118641"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>Documento de PrintCapabilities como um instantâneo das propriedades

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O dispositivo descrito pelos PrintCapabilities pode ter propriedades que dependem do Estado ou da configuração do dispositivo. Embora os PrintCapabilities representem o espaço completo de configuração de um dispositivo, o provedor de PrintCapabilities produz uma instância dependente de configuração dos recursos de PrintCapabilities chamados de documentos de PrintCapabilities. Este documento de PrintCapabilities dependente de configuração evita sobrecarregar o esquema de PrintCapabilities com a complexidade de representar dados de valores. Mais importante, para aliviar um consumidor do documento PrintCapabilities da carga de extrair o valor apropriado de uma representação de dados com valores múltiplos, todas as instâncias de propriedade e ScoredProperty em um documento de PrintCapabilities devem ser de valor único. Em outras palavras, cada instância de propriedade e ScoredProperty em um documento de PrintCapabilities deve ter um valor fixo, em relação à configuração de entrada. Cada documento de PrintCapabilities pode ser considerado um instantâneo das propriedades do dispositivo quando o dispositivo está em um estado específico. Consequentemente, antes que um documento de PrintCapabilities possa ser construído, a configuração a ser usada deve ser fornecida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



