---
title: Interfaces de esquema
description: Interfaces de esquema
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- ADSI de interfaces de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915889"
---
# <a name="schema-interfaces"></a>Interfaces de esquema

O contêiner de esquema contém um conjunto de definições de esquema que são anexadas a parte da árvore de namespace do provedor. Normalmente, cada instância de um namespace tem seu próprio esquema. Por exemplo, na figura a seguir, o provedor de exemplo ADSI define um contêiner de esquema em cada um dos nós raiz "Seattle" e "Toronto".

![contenção do esquema](images/schemacont.png)

Para criar uma implementação de ADSI para um provedor, você precisa fornecer objetos de gerenciamento de esquema que reflitam o namespace subjacente do provedor e que dão suporte a interfaces de esquema ADSI. A seguir está uma lista das interfaces de esquema ADSI, que estão contidas no contêiner de esquema.

-   [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) representa classes de serviço de diretório.
-   [**Iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) representa as propriedades do serviço de diretório que têm um ou vários valores.
-   [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) representa o tipo de variante única.

As interfaces definidas pelo ADSI podem dar suporte a propriedades e sintaxes específicas para seu provedor. Os provedores podem optar por estender uma definição de ADSI usando os métodos que criam e acessam Propriedades, por exemplo, você pode usar os métodos da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex). Os provedores também podem dar suporte a propriedades adicionais por meio de interfaces adicionais. Para obter uma lista completa de interfaces ADSI, consulte [interfaces ADSI](adsi-interfaces.md).

Um componente de provedor ADSI com um namespace complexo pode permitir que vários esquemas existam em uma instância de namespace, cada um em uma parte diferente da árvore. A propriedade [**IADs:: Schema**](iads-property-methods.md) de um objeto, no entanto, sempre nomeia sua própria definição de esquema.

 

 




