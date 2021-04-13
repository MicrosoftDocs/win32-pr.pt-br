---
title: Usando as interfaces IADs
description: ADSI, cada elemento de um serviço de diretório é representado por um objeto ADSI, que é um objeto Component Object Model (COM) que dá suporte à interface padrão COM IUnknown, bem como às interfaces IDispatch e IADs.
ms.assetid: bdbf2012-6863-4611-8173-6a3cd9c4960f
ms.tgt_platform: multiple
keywords:
- IADs ADSI, usando
- ADSI ADSI, usando, usando as interfaces IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878afa9350a45f18238bebb69df1a96eba52715e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366718"
---
# <a name="using-the-iads-interfaces"></a>Usando as interfaces IADs

ADSI, cada elemento de um serviço de diretório é representado por um objeto ADSI, que é um objeto Component Object Model (COM) que dá suporte à interface padrão COM [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , bem como às interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . **IADs** fornece as funções de manutenção básicas para objetos ADSI.

Cada objeto ADSI deve dar suporte a essa interface, que serve para:

-   Forneça a identificação de objeto por nome, classe ou ADsPath.
-   Identifique o contêiner de objeto que gerencia a criação e exclusão de objetos.
-   Obtenha a definição do esquema de objeto.
-   Carregue os atributos de objeto no cache de propriedades e confirme as alterações no repositório de diretórios persistente.
-   Acesse e modifique os valores de atributo de objeto no cache de propriedades.

A interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) foi projetada para garantir que os objetos ADSI forneçam aos administradores de rede e provedores de serviço de diretório uma representação eficiente e consistente de vários serviços de diretório subjacentes.

![objeto ADSI que dá suporte à interface IADs](images/ds2iads.png)

A figura anterior mostra um objeto ADSI genérico que dá suporte às interfaces fundamentais [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Um objeto ADSI, como isso, gerencia dados do armazenamento de dados do serviço de diretório subjacente por meio das interfaces que ele suporta. Esses dados são conhecidos como propriedades do objeto, e as rotinas que obtêm e definem essas propriedades são conhecidas como métodos de propriedade. As propriedades somente leitura têm um método de propriedade que obtém o valor da propriedade. As propriedades de leitura/gravação têm dois métodos; um método que define o valor e um que obtém o valor. As propriedades são implementadas em cada objeto ADSI usando um [cache de propriedades](the-adsi-attribute-cache.md). [**IADs:: get \_ ADsPath**](iads-property-methods.md) e **IADs::p UT \_ ADsPath** são exemplos de métodos de propriedade. Os métodos de propriedade não são aparentes para Visual Basic e outros clientes de automação que habilitam referências diretas à propriedade. Por exemplo, Visual Basic se refere a **IADs:: ADsPath** diretamente usando a sintaxe **Object. ADsPath** . Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

Além disso, um objeto ADSI interage com outros objetos ADSI e diretamente com um namespace por meio de métodos. Os métodos são executados imediatamente. Exemplos de métodos incluem [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) e [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).

Propriedades, métodos de propriedade e métodos são todos acessados por meio de interfaces COM padrão.

Um objeto ADSI é identificado exclusivamente por seu ADsPath. Por exemplo, um ADsPath para o namespace LDAP é "LDAP://MyServer/DC=Fabrikam,DC=COM". Para obter mais informações sobre ADsPaths, consulte [vinculação ADSI](binding-to-an-adsi-object.md). Para os programadores familiarizados com monikers COM, isso é conceitualmente semelhante ao nome de exibição do moniker COM.

Qualquer objeto ADSI que contenha outros objetos ADSI, chamado de objeto de contêiner ADSI, também dá suporte à interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) , que fornece métodos e propriedades que gerenciam a criação, a exclusão e a enumeração de objetos ADSI contidos no objeto. A figura a seguir mostra um objeto de contêiner ADSI.

![objeto de contêiner ADSI](images/dsiadsc.png)

A maioria dos objetos ADSI está contida em outros objetos. O único objeto ADSI sem contêiner pai é o objeto de **namespaces** ADSI de nível superior ("ads:").

O método [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) em um objeto de contêiner armazena de forma persistente as propriedades armazenadas em cache do objeto de contêiner ADSI para o armazenamento, além de quaisquer objetos criados com o método [**IADsContainer:: Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) . [**IADsContainer: o:D xcluir**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) não afeta o cache de propriedades, mas exclui o elemento de diretório de namespace subjacente representado por esse objeto.

 

 