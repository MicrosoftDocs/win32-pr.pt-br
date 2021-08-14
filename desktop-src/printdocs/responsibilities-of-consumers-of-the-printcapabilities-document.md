---
description: Os consumidores de documentos PrintCapabilities têm determinadas obrigações que devem cumprir antes de usar um documento PrintCapabilities.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilidades dos consumidores do documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49cd8f843bfa39a4313b0958fe9874f1263403e3fb3b2f22e2c965927bf6f25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470248"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>Responsabilidades dos consumidores do documento PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Os consumidores de documentos PrintCapabilities têm determinadas obrigações que devem cumprir antes de usar um documento PrintCapabilities. Os requisitos a seguir se aplicam aos clientes de um documento PrintCapabilities.

-   Eles não devem rejeitar ou não processar nenhum PrintCapabilities sintaticamente válido; ou seja, qualquer documento PrintCapabilities que esteja em conformidade com o esquema PrintCapabilities.

-   Eles devem ser capazes de resolver a presença inesperada ou a ausência de conteúdo definido de forma privada. Isso inclui conteúdo definido de forma privada que aparece em instâncias de elementos definidos pelo esquema de impressão.

-   Eles devem ser capazes de resolver o conteúdo opcional do esquema de impressão que está ausente.

-   Eles devem estar cientes de quando solicitar um novo documento.

    -   Os valores de Instâncias de propriedade dependem da configuração (portanto, dependentes de instantâneo). Você deve atualizar o instantâneo ao acessar uma instância de Propriedade.

    -   As instâncias Feature, Option e ScoredProperty que devem ser copiadas para um PrintTicket são estáticas por definição. Ou seja, eles não são (e não devem ser) dependentes da configuração do dispositivo. Se você acessar qualquer instância desses tipos, não precisará obter um novo documento PrintCapabilities quando a configuração for mudada.

-   Os consumidores de PrintCapabilities que são clientes de interface do usuário devem ser capazes de usar informações em um documento PrintCapabilities para construir uma interface do usuário e construir um PrintTicket válido com base nas seleções do usuário. Isso inclui saber quais instâncias ParameterInit devem ser especificadas e validar as instâncias especificadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



