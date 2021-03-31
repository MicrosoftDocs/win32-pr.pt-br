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
# <a name="about-the-active-directory-schema"></a>Sobre o esquema de Active Directory

Cada objeto no Active Directory Domain Services é uma instância de uma classe de objeto definida no esquema de Active Directory. Uma classe de objeto representa uma categoria de objetos, como usuários, impressoras ou programas de aplicativo, que compartilham um conjunto de características comuns. A definição para cada classe de objeto contém uma lista dos atributos que podem ser usados para descrever instâncias da classe. Por exemplo, a classe de usuário tem atributos como **o,** o **sobrenome** e o **StreetAddress**. A lista de atributos para uma classe é dividida em aqueles que um objeto dessa classe deve conter e atributos adicionais que um objeto pode conter. O diretório é organizado em uma hierarquia; a definição de cada classe também lista as classes cujos objetos podem ser pais de objetos de uma determinada classe – isso controla a forma da hierarquia de diretórios.

O esquema também define formalmente cada atributo. A definição de cada atributo inclui identificadores exclusivos para o atributo, a sintaxe do atributo (ou seja, o tipo de dados para os valores do atributo), limites de intervalo opcionais para os valores de atributo, se o atributo pode ter apenas um valor ou vários valores e se o atributo é indexado. O esquema de diretório define cada atributo exatamente uma vez — as definições de classe de objeto contêm referências aos atributos definidos no esquema. Por exemplo, o atributo "Description" é definido apenas uma vez e é referenciado por muitas classes de objeto. Isso é diferente de um esquema de banco de dados relacional, onde os "atributos" (colunas) são definidos separadamente para cada tabela.

 

 




