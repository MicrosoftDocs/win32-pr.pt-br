---
title: Acessando e manipulando dados com ADSI
description: Todos os objetos têm propriedades.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI, acessando e manipulando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3291db7490c79aae6363f619582ed24339fb83d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105748341"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Acessando e manipulando dados com ADSI

Todos os objetos têm propriedades. Todos os objetos COM da interface de serviço do Active Directory (ADSI) têm uma ou mais interfaces com métodos que recuperam as propriedades do objeto de diretório que o objeto COM representa. Há várias maneiras pelas quais você pode ler as propriedades de um objeto:

-   Obter uma propriedade específica por nome: a interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) tem dois métodos [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) para ler uma propriedade específica. Todo objeto COM ADSI tem uma interface **IADs** .
-   Obter uma lista especificada de propriedades: a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) tem o método [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) que permite especificar uma lista que contém os nomes das propriedades a serem lidas e retorna uma matriz de estruturas que contém os valores de propriedade solicitados.
-   Enumerar todas as propriedades no objeto: a interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) permite enumerar todas as propriedades em um objeto.
-   Obter propriedades especiais: as interfaces de automação ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) têm métodos de propriedade que permitem que você obtenha propriedades especiais que não são armazenadas em um objeto. Ou os métodos de propriedade podem permitir que você obtenha uma propriedade de objeto em um formato de dados diferente do tipo de dados real armazenado. Por exemplo, a interface **IADs** tem métodos de propriedade como [**IADs:: get \_ Name**](iads-property-methods.md), que recupera o RDN (nome distinto relativo) de um objeto; **IADs:: get \_ Classe**, que recupera a classe de um objeto e **IADs:: get \_ pai**, que recupera o ADsPath para o pai do objeto.

A ADSI permite que você armazene em cache as propriedades localmente depois que elas foram lidas no servidor de diretório. Isso permite que você escolha a leitura das propriedades do cache de propriedades local ou a recuperação das propriedades diretamente do servidor de diretório. A ADSI também tem métodos para atualizar o cache, bem como especificar se todas as propriedades de um objeto são armazenadas em cache ou apenas aquelas que você especificou.

Depois de recuperar uma propriedade, você lê seu valor. O tipo de dados de uma propriedade depende da definição da propriedade (também conhecida como um atributo) no esquema de Active Directory. Para cada tipo de propriedade que pode existir em Active Directory, há um objeto **attributeSchema** no esquema de Active Directory. Um objeto **attributeSchema** define as características do atributo. Uma dessas características é a sintaxe do atributo, que determina o tipo de dados dos valores do atributo. Para obter mais informações, consulte [características de atributos](/windows/desktop/AD/characteristics-of-attributes) e [sintaxes para atributos de Active Directory](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services).

As interfaces de automação ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) retornam um valor de propriedade como uma [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) ou um ponteiro para uma interface de automação em um objeto com que representa a propriedade. As interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) retornam uma propriedade como um ponteiro para uma estrutura que contém um valor de propriedade tipada ou um ponteiro para uma cadeia de caracteres de bytes. Além disso, **IDirectoryObject** e **IDirectorySearch** recuperam propriedades diretamente do servidor de diretório em vez de usar um cache de propriedades local.

Esta seção descreve os seguintes tópicos:

-   [As interfaces IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md)
-   [Acessando atributos com ADSI](accessing-attributes-with-adsi.md)
-   [Modificando atributos com ADSI](modifying-attributes-with-adsi.md)
-   [Acessando o cache de propriedades diretamente com as interfaces IADsproperty](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [Sintaxe de atributo ADSI](adsi-attribute-syntax.md)

 

 