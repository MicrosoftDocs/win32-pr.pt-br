---
title: Implementação de núcleo
description: Um provedor ADSI dá suporte aos seguintes recursos
ms.assetid: 39798237-a181-43b4-8441-ac711f923d4d
ms.tgt_platform: multiple
keywords:
- ADSI de implementação principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78487b701cac0409745ed3a7776dd882f2c37a878dec1d144c3b52a426db487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962085"
---
# <a name="core-implementation"></a>Implementação de núcleo

Um provedor ADSI oferece suporte aos seguintes recursos:

-   Cadeias de caracteres ADsPath no formato COM e URL. Por definição, você pode recuperar um objeto Active Directory usando um ADsPath. Os provedores dão suporte à sintaxe que seu serviço de diretório requer usando a implementação **ParseDisplayName** .
-   Um objeto de namespace de nível superior que dá suporte a [**IParseDisplayName::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) e [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject). Este objeto contém os nós raiz para este namespace. Parte da implementação de **ParseDisplayName** deve incluir um analisador que verifica erros de sintaxe para seu próprio namespace. Esse objeto também deve oferecer suporte a [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e **IADsOpenDSObject**.
-   A interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Isso inclui uma implementação de cache de propriedade simples por meio de [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) e [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo). As operações que Obtém ou definem propriedades de objeto ocorrem no modo cache. Os valores de cache são gravados no repositório de diretório subjacente durante **IADs:: setinfo**. No entanto, um método ADSI não é armazenado em cache, mas é executado imediatamente.
-   As interfaces [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) para acessar e enumerar diretamente as propriedades no cache de propriedades. Para serviços de diretório que não expõem um esquema, essa interface permite que você manipule as propriedades de um objeto.
-   A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para clientes que não são de automação. Isso usa o protocolo over-the-fios para obter o desempenho máximo e ignora o cache de propriedades.
-   A interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . Cada objeto de Active Directory tem um contêiner pai que controla seu tempo de vida. Lembre-se de que, para objetos de contêiner ADs, [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) afeta apenas as propriedades do contêiner e não seu conteúdo. Setinfo nos objetos de contêiner do ADs afeta apenas as propriedades do contêiner e não afeta objetos recém-criados ou objetos que já existem no contêiner.
-   A interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . essa é a interface de automação para linguagens como o Visual Basic script Edition, que não usam a associação de tempo de compilação. Relacionado a esses são os dados de biblioteca de tipos que um provedor deve fornecer. Para obter mais informações, consulte [problemas de implementação para provedores ADSI](implementation-issues-for-adsi-providers.md).
-   Um objeto de contêiner de classe de esquema e a sintaxe apropriada, a propriedade e os objetos de classe de esquema que dão suporte a [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax), [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) , respectivamente. No mínimo, cada nó raiz deve conter seu próprio objeto contêiner de classe de esquema.
-   A interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) , se quaisquer atributos com suporte forem coleções de objetos ADSI, como grupos de segurança.
-   A interface [**iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) , se quaisquer atributos com suporte forem coleções do mesmo tipo de elemento de diretório com o recurso [**iadscollection:: Add**](/windows/desktop/api/Iads/nf-iads-iadscollection-add) e [**iadscollection:: Remove**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove) .
-   A enumeração **IEnumXXXX** dá suporte a todos os objetos de enumerador específicos.
-   Rotinas para mapear a sintaxe e converter dados nativos para o tipo de dados [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .
-   Siga as convenções ADSI para objetos ADSI fornecidos pelo provedor. Inclua arquivos de ajuda e bibliotecas de tipos documentando as propriedades e métodos da interface.

Assim como ocorre com qualquer implementação de COM, as chamadas para [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) devem retornar **e \_ nointerface** para interfaces não implementadas, **e \_ NOTIMPL** para métodos não implementados de interfaces que, de outra forma, são implementadas e retornam a **\_ propriedade e ADS \_ \_ sem \_ suporte** para propriedades não implementadas. Para obter mais informações sobre interfaces duplas e como elas afetam a implementação da propriedade, consulte [interfaces duplas](dual-interfaces.md).

 

 