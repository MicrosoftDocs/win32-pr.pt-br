---
title: Interfaces de esquema
description: Interfaces de esquema
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- interfaces de esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dfa22a32a4d93c36a7419d48ea6127c2345ffdea62686147d1ba08c41ea7992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770546"
---
# <a name="schema-interfaces"></a>Interfaces de esquema

O contêiner de esquema contém um conjunto de definições de esquema anexadas a parte da árvore de namespace do provedor. Normalmente, cada instância de um namespace tem seu próprio esquema. Por exemplo, na figura a seguir, o provedor de exemplo ADSI define um contêiner de esquema em cada um dos nós raiz "Seattle" e "Toronto".

![contenção de esquema](images/schemacont.png)

Para criar uma implementação adsi para um provedor, você precisa fornecer objetos de gerenciamento de esquema que refletem o namespace subjacente do provedor e que suportam interfaces de esquema ADSI. Veja a seguir uma lista das interfaces de esquema ADSI, que estão contidas no contêiner de esquema.

-   [**IADsClass representa**](/windows/desktop/api/Iads/nn-iads-iadsclass) classes de serviço de diretório.
-   [**IADsProperty representa**](/windows/desktop/api/Iads/nn-iads-iadsproperty) propriedades de serviço de diretório que têm valores individuais ou múltiplos.
-   [**IADsSyntax representa**](/windows/desktop/api/Iads/nn-iads-iadssyntax) o único tipo VARIANT.

As interfaces definidas pelo ADSI podem dar suporte a propriedades e sintaxes específicas para seu provedor. Os provedores podem optar por estender uma definição ADSI usando os métodos que criam e acessam propriedades, por exemplo, você pode usar os métodos da interface [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) como [**Get,**](/windows/desktop/api/Iads/nf-iads-iads-get) [**GetEx,**](/windows/desktop/api/Iads/nf-iads-iads-getex) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**PutEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex) Os provedores também podem dar suporte a propriedades adicionais por meio de interfaces adicionais. Para ver uma lista completa de interfaces ADSI, consulte [Interfaces ADSI](adsi-interfaces.md).

Um componente do provedor ADSI com um namespace complexo pode permitir que vários esquemas existam em uma instância de namespace, cada um em uma parte diferente da árvore. A [**propriedade IADs::Schema**](iads-property-methods.md) de um objeto, no entanto, sempre nomeia sua própria definição de esquema.

 

 




