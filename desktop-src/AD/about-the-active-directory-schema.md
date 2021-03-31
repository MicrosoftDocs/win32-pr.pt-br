---
title: Sobre o esquema de Active Directory
description: Cada objeto no Active Directory Domain Services é uma instância de uma classe de objeto definida no esquema de Active Directory.
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822163"
---
# <a name="about-the-active-directory-schema"></a><span data-ttu-id="d0509-103">Sobre o esquema de Active Directory</span><span class="sxs-lookup"><span data-stu-id="d0509-103">About the Active Directory Schema</span></span>

<span data-ttu-id="d0509-104">Cada objeto no Active Directory Domain Services é uma instância de uma classe de objeto definida no esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0509-104">Every object in Active Directory Domain Services is an instance of an object class defined in the Active Directory schema.</span></span> <span data-ttu-id="d0509-105">Uma classe de objeto representa uma categoria de objetos, como usuários, impressoras ou programas de aplicativo, que compartilham um conjunto de características comuns.</span><span class="sxs-lookup"><span data-stu-id="d0509-105">An object class represents a category of objects, such as users, printers, or application programs, that share a set of common characteristics.</span></span> <span data-ttu-id="d0509-106">A definição para cada classe de objeto contém uma lista dos atributos que podem ser usados para descrever instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="d0509-106">The definition for each object class contains a list of the attributes that can be used to describe instances of the class.</span></span> <span data-ttu-id="d0509-107">Por exemplo, a classe de usuário tem atributos como **o,** o **sobrenome** e o **StreetAddress**.</span><span class="sxs-lookup"><span data-stu-id="d0509-107">For example, the User class has attributes such as **givenName**, **surname**, and **streetAddress**.</span></span> <span data-ttu-id="d0509-108">A lista de atributos para uma classe é dividida em aqueles que um objeto dessa classe deve conter e atributos adicionais que um objeto pode conter.</span><span class="sxs-lookup"><span data-stu-id="d0509-108">The list of attributes for a class is divided into those that an object of that class must contain, and additional attributes that an object may contain.</span></span> <span data-ttu-id="d0509-109">O diretório é organizado em uma hierarquia; a definição de cada classe também lista as classes cujos objetos podem ser pais de objetos de uma determinada classe – isso controla a forma da hierarquia de diretórios.</span><span class="sxs-lookup"><span data-stu-id="d0509-109">The directory is arranged in a hierarchy; the definition of each class also lists the classes whose objects can be parents of objects of a given class—this controls the shape of the directory hierarchy.</span></span>

<span data-ttu-id="d0509-110">O esquema também define formalmente cada atributo.</span><span class="sxs-lookup"><span data-stu-id="d0509-110">The schema also formally defines each attribute.</span></span> <span data-ttu-id="d0509-111">A definição de cada atributo inclui identificadores exclusivos para o atributo, a sintaxe do atributo (ou seja, o tipo de dados para os valores do atributo), limites de intervalo opcionais para os valores de atributo, se o atributo pode ter apenas um valor ou vários valores e se o atributo é indexado.</span><span class="sxs-lookup"><span data-stu-id="d0509-111">The definition for each attribute includes unique identifiers for the attribute, the syntax for the attribute (that is, the data type for the attribute's values), optional range limits for the attribute values, whether the attribute can have only one value or multiple values, and whether the attribute is indexed.</span></span> <span data-ttu-id="d0509-112">O esquema de diretório define cada atributo exatamente uma vez — as definições de classe de objeto contêm referências aos atributos definidos no esquema.</span><span class="sxs-lookup"><span data-stu-id="d0509-112">The directory schema defines each attribute exactly once—object class definitions contain references to the attributes defined in the schema.</span></span> <span data-ttu-id="d0509-113">Por exemplo, o atributo "Description" é definido apenas uma vez e é referenciado por muitas classes de objeto.</span><span class="sxs-lookup"><span data-stu-id="d0509-113">For example, the "description" attribute is defined only once and is referenced by many object classes.</span></span> <span data-ttu-id="d0509-114">Isso é diferente de um esquema de banco de dados relacional, onde os "atributos" (colunas) são definidos separadamente para cada tabela.</span><span class="sxs-lookup"><span data-stu-id="d0509-114">This is different than a relational database schema, where the "attributes" (columns) are separately defined for each table.</span></span>

 

 




