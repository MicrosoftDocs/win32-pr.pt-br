---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilidades de consumidores do documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105787727"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>Responsabilidades de consumidores do documento de PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Os consumidores de documentos de PrintCapabilities têm determinadas obrigações que devem ser suspensos antes que possam usar um documento de PrintCapabilities. Os requisitos a seguir se aplicam aos clientes de um documento PrintCapabilities.

-   Eles não devem rejeitar ou não processar nenhum recurso de PrintCapabilities sintaticamente válido; ou seja, qualquer documento de PrintCapabilities que esteja de acordo com o esquema de PrintCapabilities.

-   Eles devem ser capazes de contornar a presença inesperada ou a ausência de conteúdo definido de modo privado. Isso inclui conteúdo definido de modo privado que aparece em instâncias de elementos de impressão definidos pelo esquema.

-   Eles devem ser capazes de contornar o conteúdo de esquema de impressão opcional que está ausente.

-   Eles devem estar cientes de quando solicitar um novo documento.

    -   Os valores das instâncias de propriedade são dependentes de configuração (portanto, dependente de instantâneo). Você deve atualizar o instantâneo ao acessar uma instância de propriedade.

    -   As instâncias Feature, Option e ScoredProperty que devem ser copiadas para um PrintTicket são por definição estática. Ou seja, eles não são (e não devem ser) dependentes da configuração do dispositivo. Se você acessar qualquer instância desses tipos, não será necessário obter um novo documento de PrintCapabilities quando a configuração for alterada.

-   Os consumidores de PrintCapabilities que são clientes da interface do usuário (IU) devem ser capazes de usar informações em um documento de PrintCapabilities para construir uma interface do usuário e construir um PrintTicket válido a partir das seleções do usuário. Isso inclui saber quais instâncias de ParameterInit devem ser especificadas e validar as instâncias especificadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



