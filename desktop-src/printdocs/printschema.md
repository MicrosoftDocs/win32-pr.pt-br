---
description: O esquema de impressão e as tecnologias relacionadas estão disponíveis no Microsoft .NET Framework 3,0 e em versões posteriores do Microsoft .NET Framework e no Windows Vista e em versões posteriores do Windows.
ms.assetid: 98d5f8ec-54bd-4e88-b632-ed427b599cb6
title: Imprimir esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3ac50b9a2f2aba9cda7dc73f183e1f3571cc9d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105761991"
---
# <a name="print-schema"></a>Imprimir esquema

O esquema de impressão e as tecnologias relacionadas estão disponíveis no Microsoft .NET Framework 3,0 e em versões posteriores do Microsoft .NET Framework e no Windows Vista e em versões posteriores do Windows. Os documentos XPS e o modelo de objeto XPS podem usar os objetos de tíquete de impressão, que são descritos na [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip), para especificar as preferências de impressão de um documento para impressoras e para exibir aplicativos.

A [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) é um documento que pode ser baixado que contém informações sobre o esquema de impressão e como usá-lo em documentos e impressão. Informações adicionais são fornecidas online apenas para suas informações, em [referência de esquema de impressão herdado](print-schema.md); no entanto, ele pode não refletir com precisão a versão atual da [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). Consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) para obter as informações de design mais atuais.

## <a name="print-schema-overview"></a>Visão geral do esquema de impressão

O esquema de impressão é um esquema baseado em XML, hierarquicamente estruturado, usado para organizar e descrever as propriedades de uma impressora ou de um trabalho de impressão. O esquema de impressão inclui dois componentes: as palavras-chave do esquema de impressão e a estrutura de esquema de impressão. As palavras-chave do esquema de impressão são um conjunto de instâncias de elemento que descrevem atributos de impressora e a intenção de formatação do trabalho de impressão. A estrutura de esquema de impressão define uma coleção hierarquicamente estruturada de tipos de elemento XML e como esses tipos de elementos podem ser usados juntos.

As tecnologias de esquema de impressão, chamadas de *PrintCapabilities* e *PrintTicket*, são criadas usando as palavras-chave do esquema de impressão, conforme especificado pela estrutura de esquema de impressão. A especificação de esquema de impressão dá suporte a extensões de esquema por terceiros, para que os usuários do esquema de impressão não sejam restritos às instâncias de propriedade, recurso, opção ou ParameterInit definidas pelas palavras-chave do esquema de impressão. As instâncias de elemento de terceiros podem ser adicionadas às instâncias de elemento que são definidas pelas palavras-chave do esquema de impressão; no entanto, as instâncias de propriedade de terceiros privadas devem pertencer a um namespace que está claramente associado a terceiros que criou o namespace.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Referência de esquema de impressão herdado](print-schema.md)
</dt> <dt>

[Comunicações bidirecionais de impressora (centro de desenvolvimento de hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

 

 
