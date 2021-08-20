---
description: Entenda os parâmetros no documento PrintCapabilities. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parâmetros no documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a2d88e75372cfc2f1301c630116c12510b37c91aadbf94a04ac07a3f4906cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867988"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Parâmetros no documento PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Conforme discutido em Elementos de Referência de Parâmetro [,](parameter-reference-elements.md)os elementos ParameterInit podem ser referenciados de dentro de instâncias option, mas o constructo de parâmetro também tem um uso que é independente desse tipo de elemento.

Um exemplo de um atributo de configuração de dispositivo que é adequado para a representação de parâmetro é CopyCount. Os valores permitidos para esse atributo de configuração de dispositivo podem ser definidos de forma fácil e concisa sem listar cada um deles explicitamente. Embora seja possível, embora entediante, listar cada valor copyCount em sua própria Opção, alguns atributos de configuração de dispositivo simplesmente não podem ser representados usando um constructo Recurso/Opção. Por exemplo, considere um dispositivo que aceita uma cadeia de caracteres de texto que é usada para produzir uma marca-d'água virtual em cada página de saída. O conjunto de todas as cadeias de caracteres de texto possíveis não pode ser enumerado explicitamente com facilidade, mas a cadeia de caracteres de texto pode ser facilmente descrita usando um elemento ParameterDef.

O documento Palavras-chave de esquema de impressão define uma série de constructos de parâmetros comumente usados, mas os provedores PrintCapabilities são livres para definir outros próprios. No entanto, esses constructos de parâmetro definidos de forma privada não são portáteis para outros dispositivos, devido ao fato de que um documento PrintCapabilities fornecido por outra parte não define esse constructo de parâmetro. Se definido pelo esquema ou definido de forma privada, a instância parameterDef deve estar presente no documento PrintCapabilities antes que o parâmetro seja reconhecido e usado pelos clientes. Esses parâmetros são chamados de *parâmetros designados.*

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



