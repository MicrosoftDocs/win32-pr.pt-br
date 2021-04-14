---
title: Documento como um instantâneo das propriedades
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73fc190ed8c259e64fdd60cc291c6ae5b58f80
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104370832"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>Documento de PrintCapabilities como um instantâneo das propriedades

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O dispositivo descrito pelos PrintCapabilities pode ter propriedades que dependem do Estado ou da configuração do dispositivo. Embora os PrintCapabilities representem o espaço completo de configuração de um dispositivo, o provedor de PrintCapabilities produz uma instância dependente de configuração dos recursos de PrintCapabilities chamados de documentos de PrintCapabilities. Este documento de PrintCapabilities dependente de configuração evita sobrecarregar o esquema de PrintCapabilities com a complexidade de representar dados de valores. Mais importante, para aliviar um consumidor do documento PrintCapabilities da carga de extrair o valor apropriado de uma representação de dados com valores múltiplos, todas as instâncias de propriedade e ScoredProperty em um documento de PrintCapabilities devem ser de valor único. Em outras palavras, cada instância de propriedade e ScoredProperty em um documento de PrintCapabilities deve ter um valor fixo, em relação à configuração de entrada. Cada documento de PrintCapabilities pode ser considerado um instantâneo das propriedades do dispositivo quando o dispositivo está em um estado específico. Consequentemente, antes que um documento de PrintCapabilities possa ser construído, a configuração a ser usada deve ser fornecida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



