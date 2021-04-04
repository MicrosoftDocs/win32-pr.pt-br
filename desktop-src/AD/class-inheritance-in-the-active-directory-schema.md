---
title: Herança de classe no esquema de Active Directory
description: Todas as classes de objeto em um esquema de serviço de diretório Active Directory são derivadas da classe especial Top.
ms.assetid: 26e5107f-8204-4f64-bd07-b5b4f16103f4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd550a3eed6aeb633f6db265260b6c65c17f993
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007354"
---
# <a name="class-inheritance-in-the-active-directory-schema"></a>Herança de classe no esquema de Active Directory

Todas as classes de objeto em um esquema de serviço de diretório Active Directory são derivadas da classe especial [**Top**](/windows/desktop/ADSchema/c-top). Com a exceção de **Top**, todas as classes de objeto são subclasses de outra classe de objeto. Por exemplo, [**Contact**](/windows/desktop/ADSchema/c-contact) é uma subclasse de [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson); **OrganizationalPerson** é uma subclasse de [**Person**](/windows/desktop/ADSchema/c-person); e **Person** é uma subclasse de **Top**. O atributo [**listas SubClassOf**](/windows/desktop/ADSchema/a-subclassof) de um objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) é uma propriedade de valor único que indica a superclasse imediata da classe.

Alguns dos valores de atributo que definem uma classe são herdados de suas superclasses. Portanto, a classe [**Contact**](/windows/desktop/ADSchema/c-contact) herda valores de suas superclasses, que são as classes [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson), [**Person**](/windows/desktop/ADSchema/c-person)e [**Top**](/windows/desktop/ADSchema/c-top) . Uma classe herda os seguintes dados de suas superclasses:

-   Atributos possíveis: os valores dos atributos [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)e [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain) de um objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) definem uma lista completa dos atributos que podem ser definidos em uma instância da classe de objeto. Para cada classe de objeto, os valores desses atributos incluem todos os valores que são herdados de suas superclasses, bem como quaisquer valores que são definidos explicitamente para a própria classe de objeto. Assim, o atributo [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) da classe [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson) inclui todos os valores **de mustContain** que são herdados das classes [**Person**](/windows/desktop/ADSchema/c-person) e [**Top**](/windows/desktop/ADSchema/c-top) , bem como os valores **mustContain** que são definidos explicitamente na classe **OrganizationalPerson** .
-   Possíveis pais na hierarquia de diretório: os valores dos atributos [**possSuperior**](/windows/desktop/ADSchema/a-posssuperiors) e [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) de um objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) definem uma lista completa das classes de objeto que podem conter uma instância da classe de objeto. Para cada classe de objeto, os valores incluem aqueles herdados de suas superclasses, bem como aqueles definidos explicitamente para a própria classe de objeto.

Lembre-se de que a classe de objeto também pode ter muitas classes auxiliares, que são especificadas nos atributos [**auxiliaryClass**](/windows/desktop/ADSchema/a-auxiliaryclass) e [**systemAuxiliaryClass**](/windows/desktop/ADSchema/a-systemauxiliaryclass) de um objeto **classSchema** . Uma classe de objeto herda os valores [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)e [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain) de suas classes auxiliares.

 

 