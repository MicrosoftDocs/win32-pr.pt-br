---
title: Definição de diretório
description: O componente de provedor de exemplo usa um design de diretório relativamente simples para esclarecer a relação entre componentes e mostrar os requisitos mínimos necessários para ser um provedor ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8a46ee47bfa280fb9cffce32480fdad3164a648eee59a0c0b2740834b1f21cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691940"
---
# <a name="directory-definition"></a>Definição de diretório

O componente de provedor de exemplo usa um design de diretório relativamente simples para esclarecer a relação entre componentes e mostrar os requisitos mínimos necessários para ser um provedor ADSI.

O "diretório" para o componente do provedor de exemplo consiste em dois nós raiz: "Seattle" e "Toronto". Seattle contém mais dois subníveis, "Bellevue" e "Redmond". Cada uma dessas entradas contém várias contas de usuário. A entrada "Toronto" não tem mais subníveis, mas contém diretamente várias contas de usuário. A figura a seguir mostra esses dois nós raiz conectados a uma rede.

![definição de diretório](images/dssmdo.png)

Em termos hierárquicos, o nó Namespace contém "Seattle" e "Toronto". "Seattle" contém "Bellevue" e "Redmond". "Bellevue" e "Redmond" contêm um conjunto de contas de usuário. "Toronto" contém diretamente as contas de usuário sem nós organizacionais intermediários.

O componente de provedor de exemplo representa essa estrutura com apenas dois tipos de objeto do Active Directory: um objeto de contêiner e um objeto folha. "Seattle", "Toronto", "Bellevue" e "Redmond" são objetos de contêiner e cada conta de usuário é um objeto folha.

O componente de provedor de exemplo cria uma classe de esquema chamada "Unidade Organizacional" para um tipo de objeto de contêiner e uma classe de esquema chamada "Usuário" para uma conta de usuário.

As propriedades de cada classe de esquema, seus métodos e as regras que regem as relações de contenção para esses objetos são definidas em [Gerenciamento de Esquema](schema-management.md).

 

 




