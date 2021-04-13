---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parâmetros no documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298015"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Parâmetros no documento PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Como discutido em [elementos de referência de parâmetro](parameter-reference-elements.md), elementos ParameterInit podem ser referenciados de dentro de instâncias de opção, mas a construção de parâmetro também tem um uso que é independente desse tipo de elemento.

Um exemplo de um atributo de configuração de dispositivo que é adequado para a representação de parâmetro é CopyCount. Os valores permitidos para esse atributo de configuração de dispositivo podem ser facilmente e concisamente definidos sem listar cada um deles explicitamente. Embora seja possível, embora entediante, listar cada valor de CopyCount em sua própria opção, alguns atributos de configuração de dispositivo simplesmente não podem ser representados usando uma construção de recurso/opção. Como exemplo, considere um dispositivo que aceita uma cadeia de caracteres de texto que é usada para produzir uma marca d' água virtual em cada página de saída. O conjunto de todas as cadeias de caracteres de texto possíveis não pode ser facilmente enumerado explicitamente, mas a cadeia de caracteres de texto pode ser facilmente descrita usando um elemento ParameterDef.

O documento de palavras-chave do esquema de impressão define uma série de construções de parâmetro usadas com frequência, mas os provedores de PrintCapabilities são livres para definir as próprias próprias. No entanto, essas construções de parâmetro definidas de forma privada não são portáveis para outros dispositivos, devido ao fato de que um documento de PrintCapabilities fornecido por outra parte não define tal constructo de parâmetro. Independentemente da definição de esquema ou definida de modo privado, a instância ParameterDef deve estar presente no documento PrintCapabilities antes que o parâmetro seja reconhecido e usado pelos clientes. Esses parâmetros são chamados de *parâmetros designados*.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



