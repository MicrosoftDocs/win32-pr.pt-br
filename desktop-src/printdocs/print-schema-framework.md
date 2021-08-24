---
description: Esses artigos fornecem informações mais detalhadas sobre o significado e o uso dos tipos de elemento Esquema de Impressão.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Estrutura de esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 986308ae2ce1308c7df090da295f8b5473efe99219339a906490299ec33b2ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718596"
---
# <a name="print-schema-framework"></a>Estrutura de esquema de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Esta seção fornece informações mais detalhadas sobre o significado e o uso dos tipos de elemento Esquema de Impressão. O foco principal da versão inicial do Print Schema Framework é representar configurações e funcionalidades de atributos de dispositivo. Em um alto nível, essa estrutura oferece dois estilos diferentes de descrever um atributo de dispositivo: como um constructo de Recurso/Opção ou como um constructo de parâmetro. Se um atributo de dispositivo tiver um pequeno número de valores ou estados disponíveis, o atributo deverá ser caracterizado como um Recurso com os valores ou estados permitidos chamados de elementos Option. Por outro lado, se um atributo de dispositivo tiver um grande número de valores ou estados disponíveis e o conjunto de todos os valores possíveis for facilmente definido sem recorrer à enumeração explícita, o atributo do dispositivo deverá ser caracterizado como um parâmetro. (Um parâmetro é definido por meio de um elemento ParameterDef e uma instância de parâmetro é inicializada por meio de um elemento ParameterInit.) Os elementos de propriedade são usados em constructos de recurso/opção e parâmetro para fornecer um nível mais fino de diferenciação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



