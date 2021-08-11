---
title: Acessando e manipulando dados com ADSI
description: Todos os objetos têm propriedades.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , acessando e manipulando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ed09c1717f4f9a9c1c75372e7efdc23d2cce1adb39242197346061ae4df00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181626"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Acessando e manipulando dados com ADSI

Todos os objetos têm propriedades. Todos os objetos COM da ADSI (Interface de Serviço do Active Directory) têm uma ou mais interfaces com métodos que recuperam as propriedades do objeto de diretório que o objeto COM representa. Há várias maneiras de ler propriedades de um objeto:

-   Obter uma propriedade específica por nome: a interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) tem dois métodos [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) para ler uma propriedade específica. Cada objeto COM ADSI tem uma interface **IADs.**
-   Obter uma lista especificada de propriedades: a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) tem o método [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) que permite especificar uma lista que contém os nomes das propriedades a ler e retorna uma matriz de estruturas que contém os valores de propriedade solicitados.
-   Enumerar todas as propriedades no objeto: a interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) permite enumerar todas as propriedades em um objeto .
-   Obter propriedades especiais: as INTERFACEs de Automação ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads)) têm métodos de propriedade que permitem obter propriedades especiais que não \* são armazenadas em um objeto . Ou os métodos de propriedade podem permitir que você receba uma propriedade de objeto em um formato de dados diferente do tipo de dados real armazenado. Por exemplo, a interface **IADs** tem métodos de propriedade como [**IADs::get \_ Name**](iads-property-methods.md), que recupera o RDN (nome diferenciado relativo) de um objeto; **IADs::get \_ Classe**, que recupera a classe de um objeto e **IADs::get \_ Parent**, que recupera o ADsPath para o pai do objeto.

A ADSI permite armazenar em cache as propriedades localmente depois que elas foram lidas do servidor de diretório. Isso permite que você escolha ler as propriedades do cache de propriedades local ou recuperar as propriedades diretamente do servidor de diretório. A ADSI também tem métodos para atualizar o cache, bem como especificar se todas as propriedades de um objeto são armazenadas em cache ou apenas aquelas especificadas.

Depois de recuperar uma propriedade, leia seu valor. O tipo de dados de uma propriedade depende da definição da propriedade (também conhecida como atributo) no esquema do Active Directory. Para cada tipo de propriedade que pode existir no Active Directory, há um **objeto attributeSchema** no esquema do Active Directory. Um **objeto attributeSchema** define as características do atributo. Uma dessas características é a sintaxe do atributo, que determina o tipo de dados dos valores do atributo. Para obter mais informações, consulte [Características de atributos](/windows/desktop/AD/characteristics-of-attributes) [e sintaxes para atributos do Active Directory](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services).

As INTERFACEs de Automação ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads)) retornam um valor da propriedade como VARIANT ou um ponteiro para uma interface de Automação em um \* objeto COM que representa a propriedade . [](/windows/win32/api/oaidl/ns-oaidl-variant) As interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) retornam uma propriedade como um ponteiro para uma estrutura que contém um valor da propriedade digitada ou um ponteiro para uma cadeia de caracteres de bytes. Além disso, **IDirectoryObject** e **IDirectorySearch** recuperam propriedades diretamente do servidor de diretório em vez de usar um cache de propriedade local.

Esta seção descreve os seguintes tópicos:

-   [As interfaces IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md)
-   [Acessando atributos com ADSI](accessing-attributes-with-adsi.md)
-   [Modificando atributos com ADSI](modifying-attributes-with-adsi.md)
-   [Acessando o cache de propriedades diretamente com as interfaces IADsProperty](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [Sintaxe de atributo ADSI](adsi-attribute-syntax.md)

 

 