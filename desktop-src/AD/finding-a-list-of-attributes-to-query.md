---
title: Localizar uma lista de atributos a consultar
description: Ao pesquisar objetos de uma classe específica, as comparações no filtro de pesquisa devem especificar atributos que realmente existem nos objetos dessa classe.
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- Localizar uma lista de atributos para consultar o AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0edfee59c42a8cf07be05ab31e58c0298f7285c8a02de659257e3b3cd14bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189186"
---
# <a name="finding-a-list-of-attributes-to-query"></a>Localizar uma lista de atributos a consultar

Ao pesquisar objetos de uma classe específica, as comparações no filtro de pesquisa devem especificar atributos que realmente existem nos objetos dessa classe. Para obter os atributos de lista em um objeto de uma classe específica, a bind a essa classe no esquema abstrato e recupere as propriedades [**IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) e **IADsClass.OptionalProperties.** Para obter mais informações, consulte [Lendo o esquema abstrato](reading-the-abstract-schema.md).

Além disso, todos os objetos herdam da classe abstrata superior. Portanto, qualquer atributo na **parte** superior pode existir, embora não possa ser definido, em nenhum objeto.

Se estiver pesquisando o catálogo global, verifique se você especificou atributos no catálogo global. Os atributos incluídos no catálogo global têm **isMemberOfPartialAttributeSet** definido como **TRUE** em seus **objetos attributeSchema.** Esteja ciente de que esses dados não estão disponíveis no esquema abstrato; lê-lo do **objeto attributeSchema** no contêiner de esquema.

No catálogo global, um atributo de link voltar poderá ser consultado somente se ambas as seguintes condições são atendidas: Primeiro, o atributo é marcado para inclusão no catálogo global. Em segundo lugar, o link de encaminhamento correspondente também é marcado para inclusão no catálogo global. Isso se aplica aos filtros de consulta, bem como aos resultados da consulta. Para obter mais informações, consulte [Atributos vinculados.](linked-attributes.md)

Além disso, alguns atributos, principalmente no objeto de usuário, são construídos. Os filtros de consulta não podem conter atributos construídos. Atributos construídos não podem ser avaliados em filtros de consulta; no entanto, eles podem ser retornados nos resultados da consulta. Isso se aplica a todos os contextos de nomeação e ao catálogo global. Atributos construídos têm **ADS \_ SYSTEMFLAG \_ ATTR \_ É \_** CONSTRUÍDO (0x00000004) na propriedade **systemFlags** em seus **objetos attributeSchema.**

> [!Note]  
> Para obter mais informações sobre classes predefinidas e atributos incluídos com o sistema, [consulte Active Directory Domain Services Reference](active-directory-domain-services-reference.md). Essas páginas listam atributos obrigatórios e opcionais de cada classe de objeto. Para atributos, a página de referência indica se o atributo é indexado, construído, vinculado ou no catálogo global.

 

 

 