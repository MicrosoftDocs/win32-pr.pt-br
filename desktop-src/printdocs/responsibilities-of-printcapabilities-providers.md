---
description: Os provedores PrintCapabilities devem dar suporte a um conjunto mínimo de recursos, que são implícitos pela Interface do Provedor PrintTicket/PrintCapabilities.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilidades dos provedores PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404909"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>Responsabilidades dos provedores PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Os provedores PrintCapabilities devem dar suporte a um conjunto mínimo de recursos, que são implícitos pela Interface do Provedor PrintTicket/PrintCapabilities. Essas funcionalidades estão listadas aqui.

-   Eles devem seguir a direção da propagação?? Atributo XML, quando ele aparece no contexto apropriado e contém um valor válido para esse contexto.

-   Eles devem gerar um documento PrintCapabilities que esteja em conformidade com o esquema PrintCapabilities e atenda aos requisitos especificados no Esquema de Impressão.

-   Eles devem ser capazes de reconhecer um PrintTicket válido.

-   Eles devem ser capazes de interpretar um PrintTicket e entender a configuração específica que ele representa.

-   Eles devem ser capazes de determinar se essa configuração contém conflitos de restrição.

-   Eles devem ser capazes de modificar um PrintTicket inválido ou conflitante fazendo a alteração menos significativa necessária para torná-la válida e sem conflitos.

-   Eles devem ser capazes de gerar um documento PrintCapabilities para uma configuração de dispositivo específica.

-   Eles devem ser capazes de gerar uma configuração padrão ou PrintTicket.

-   Eles devem ser capazes de gerar um documento PrintCapabilities que corresponda à configuração padrão.

-   Eles devem implementar um processo de pontuação de opção definido pelo driver de dispositivo capaz de determinar a proximidade da combinação entre duas instâncias option que pertencem ao mesmo recurso. Esse algoritmo é usado no processo de validação printTicket.

Além dos requisitos acima, o documento PrintCapabilities deve conter valores válidos e corretos para cada atributo XML (por exemplo, restrito) de cada Opção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



