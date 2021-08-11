---
description: Saiba mais sobre os usos de PrintCapabilities. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usos dos PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96aec2d21a2751305ae1f2e191a37adb584a0209542a78a0bf53253ea66faa20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233524"
---
# <a name="uses-of-the-printcapabilities"></a>Usos dos PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

As PrintCapabilities são destinadas a representar atributos de dispositivo configuráveis como construções de recurso/opção ou construções de parâmetro. Essas informações definem o espaço de configuração do dispositivo e podem ser usadas por um cliente de interface do usuário (IU) para construir uma IU. As palavras-chave do esquema de impressão definem um conjunto de instâncias de recursos padrão, instâncias de opção para as instâncias de recurso padrão e instâncias de ParameterDef.

As construções de recurso/opção ou parâmetro nos recursos de PrintCapabilities destinam-se a manter as instâncias de propriedade ou ScoredProperty que descrevem um dispositivo e que têm suporte no subsistema do spooler. Essas instâncias de propriedade e ScoredProperty são de interesse geral para clientes do dispositivo e contêm as informações fornecidas pelas funções do DevCaps do Win32. As palavras-chave do esquema de impressão definem um conjunto de propriedades padrão e instâncias de ScoredProperty.

Deve-se enfatizar que o documento de PrintCapabilities tem como objetivo representar apenas dados de valor único: dados que não dependem de uma configuração específica do dispositivo. O documento PrintCapabilities fornece apenas um instantâneo dos dados dependentes de configuração.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



