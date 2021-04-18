---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instâncias de propriedade importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105791085"
---
# <a name="important-property-instances"></a>Instâncias de propriedade importantes

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Para que um cliente de PrintCapabilities possa construir um PrintTicket razoável, o documento PrintCapabilities deve fornecer certas propriedades de instâncias de recursos, bem como instâncias de opção dentro do recurso. Um módulo de interface do usuário genérica (IU) requer essas informações para construir uma interface do usuário. Isso, por sua vez, requer que as palavras-chave do esquema de impressão definam algumas instâncias de propriedade que aparecem como filhos dos elementos Feature e Option.

Os elementos de recurso podem conter a seguinte propriedade.



| Propriedade                  | Valores                                 | Finalidade                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SelectionType <br/> | PickOne<br/> PickMany<br/> | Especifica o número de opções que podem ser selecionadas para esse recurso em um determinado momento, qualquer um (PickOne) ou mais de um (PickMany). O cliente pode usar essas informações para construir um PrintTicket. Essas informações afetam o comportamento da interface do usuário, bem como a validação de PrintTicket pelo provedor.<br/> |



 

Os elementos de opção podem conter a propriedade a seguir.



| Propriedade                   | Valores                           | Finalidade                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IdentityOption <br/> | True<br/> Falso<br/> | A seleção da propriedade IdentityOption é interpretada para significar "desabilitar este recurso". Um recurso que contém uma Propriedade SelectionType cujo valor é PickMany também deve conter uma opção que tem uma propriedade IdentityOption. O código da interface do usuário (ou cliente construindo um PrintTicket) deve anular a seleção de qualquer outra opção se a propriedade IdentityOption estiver selecionada.<br/> |



 

Os elementos Feature, Option e ParameterDef podem conter a propriedade a seguir.



| Propriedade              | Valores                          | Finalidade                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayUI <br/> | Mostrar<br/> Ocultar<br/> | Especifica se o elemento pai deve ser exibido na interface do usuário. Mostrar indica que o elemento deve ser exibido na interface do usuário. Ocultar indica que o elemento não deve ser exibido na interface do usuário. Se essa propriedade não for definida para um elemento, a interpretação padrão será mostrada, o que significa que o elemento é exibido.<br/> |



 

Os elementos Feature, Option e ParameterDef podem conter a propriedade a seguir.



| Propriedade                | Valor             | Finalidade                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName <br/> | String<br/> | Especifica a cadeia de caracteres de exibição para o elemento pai, substituindo o nome de exibição padrão. Pode ser usado por provedores de PrintCapabilities para apresentar um nome de exibição localizado e amigável. O valor do nome de exibição padrão é o atributo Name para o elemento pai. <br/> No caso de elementos Option, se o atributo Name não for fornecido, a propriedade DisplayName deverá estar presente.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




