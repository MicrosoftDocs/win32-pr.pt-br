---
title: Localizando uma lista de atributos a serem consultados
description: Ao pesquisar objetos de uma determinada classe, as comparações no filtro de pesquisa devem especificar atributos que realmente existem nos objetos dessa classe.
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- Localizando uma lista de atributos para consultar o AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b6fb6b4d948a7cbc4d76caba9b78e189324eaa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640403"
---
# <a name="finding-a-list-of-attributes-to-query"></a>Localizando uma lista de atributos a serem consultados

Ao pesquisar objetos de uma determinada classe, as comparações no filtro de pesquisa devem especificar atributos que realmente existem nos objetos dessa classe. Para obter os atributos de lista em um objeto de uma determinada classe, associe a essa classe no esquema abstrato e recupere as propriedades [**IADsClass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) e **IADsClass. OptionalProperties** . Para obter mais informações, consulte [lendo o esquema abstrato](reading-the-abstract-schema.md).

Além disso, todos os objetos herdam da classe abstrata top. Portanto, qualquer atributo no **topo** pode existir, embora não seja definido, em nenhum objeto.

Se pesquisar o catálogo global, certifique-se de especificar atributos no catálogo global. Os atributos incluídos no catálogo global têm o **isMemberOfPartialAttributeSet** definido como **true** em seus objetos **attributeSchema** . Lembre-se de que esses dados não estão disponíveis no esquema abstrato; Leia-o no objeto **attributeSchema** no contêiner de esquema.

No catálogo global, um atributo de vínculo regressivo pode ser consultado somente se ambas as condições a seguir forem atendidas: primeiro, o atributo será marcado para inclusão no catálogo global. Em segundo lugar, o link de encaminhamento correspondente também é marcado para inclusão no catálogo global. Isso se aplica aos filtros de consulta, bem como aos resultados da consulta. Para obter mais informações, consulte [atributos vinculados](linked-attributes.md).

Além disso, alguns atributos, principalmente no objeto de usuário, são construídos. Os filtros de consulta não podem conter atributos construídos. Atributos construídos não podem ser avaliados em filtros de consulta; no entanto, eles podem ser retornados nos resultados da consulta. Isso se aplica a todos os contextos de nomenclatura e ao catálogo global. Os atributos construídos têm o **\_ atributo SYSTEMFLAG \_ attr \_ \_ construído** (0x00000004) na propriedade **systemFlags** em seus objetos **attributeSchema** .

> [!Note]  
> Para obter mais informações sobre classes e atributos predefinidos incluídos no sistema, consulte [referência de Active Directory Domain Services](active-directory-domain-services-reference.md). Essas páginas listam atributos obrigatórios e opcionais de cada classe de objeto. Para atributos, a página de referência indica se o atributo é indexado, construído, vinculado ou no catálogo global.

 

 

 