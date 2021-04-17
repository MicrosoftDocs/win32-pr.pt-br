---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilidades de provedores de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763769"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>Responsabilidades de provedores de PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Os provedores de PrintCapabilities devem dar suporte a um conjunto mínimo de recursos, que são implícitos pela interface do provedor PrintTicket/PrintCapabilities. Esses recursos estão listados aqui.

-   Eles devem seguir a direção da propagação?? O atributo XML, quando aparece no contexto apropriado, e contém um valor válido para esse contexto.

-   Eles devem gerar um documento de PrintCapabilities que esteja de acordo com o esquema de PrintCapabilities e atenda aos requisitos especificados no esquema de impressão.

-   Eles devem ser capazes de reconhecer um PrintTicket válido.

-   Eles devem ser capazes de interpretar um PrintTicket e compreender a configuração específica que ele representa.

-   Eles devem ser capazes de determinar se essa configuração contém conflitos de restrição.

-   Eles devem ser capazes de modificar um PrintTicket inválido ou conflitante, tornando a alteração menos significativa necessária para torná-lo válido e sem conflitos.

-   Eles devem ser capazes de gerar um documento de PrintCapabilities para uma configuração de dispositivo específica.

-   Eles devem ser capazes de gerar uma configuração padrão ou PrintTicket.

-   Eles devem ser capazes de gerar um documento de PrintCapabilities que corresponda à configuração padrão.

-   Eles devem implementar um processo de Pontuação de opção definido pelo driver de dispositivo capaz de determinar a proximidade de correspondência entre duas instâncias de opção que pertencem ao mesmo recurso. Esse algoritmo é usado no processo de validação do PrintTicket.

Além dos requisitos acima, o documento PrintCapabilities deve conter valores válidos e corretos para cada atributo XML (por exemplo, restrito) de cada opção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



