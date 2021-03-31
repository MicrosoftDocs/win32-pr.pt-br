---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Estrutura de esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617f747b950676f2359645684c9e672fb5c87ee3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172530"
---
# <a name="print-schema-framework"></a>Estrutura de esquema de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Esta seção fornece informações mais detalhadas sobre o significado e o uso dos tipos de elemento de esquema de impressão. O foco principal da versão inicial da estrutura de esquema de impressão é representar as configurações e os recursos dos atributos do dispositivo. Em um alto nível, essa estrutura oferece dois estilos diferentes de descrição de um atributo de dispositivo: como um constructo de recurso/opção ou como uma construção de parâmetro. Se um atributo de dispositivo tiver um pequeno número de valores ou Estados disponíveis, o atributo deverá ser caracterizado como um recurso com os valores permitidos ou Estados chamados de elementos de opção. Por outro lado, se um atributo de dispositivo tiver um grande número de valores ou Estados disponíveis e o conjunto de todos os valores possíveis for facilmente definido sem recorrer à enumeração explícita, o atributo do dispositivo deverá ser caracterizado como um parâmetro. (Um parâmetro é definido por meio de um elemento ParameterDef e uma instância de parâmetro é inicializada por meio de um elemento ParameterInit.) Os elementos de propriedade são usados em constructos de recurso/opção e de parâmetro para fornecer um nível mais preciso de diferenciação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



