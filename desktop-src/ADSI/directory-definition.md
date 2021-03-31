---
title: Definição de diretório
description: O componente de provedor de exemplo usa um design de diretório relativamente simples para esclarecer a relação entre componentes e mostrar os requisitos mínimos necessários para ser um provedor ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822222"
---
# <a name="directory-definition"></a>Definição de diretório

O componente de provedor de exemplo usa um design de diretório relativamente simples para esclarecer a relação entre componentes e mostrar os requisitos mínimos necessários para ser um provedor ADSI.

O "diretório" para o componente de provedor de exemplo consiste em dois nós raiz: "Seattle" e "Toronto". Seattle contém mais dois subníveis, "Bellevue" e "Redmond". Cada uma dessas entradas contém várias contas de usuário. A entrada "Toronto" não tem mais subníveis, mas contém diretamente várias contas de usuário. A figura a seguir mostra esses dois nós raiz conectados a uma rede.

![definição de diretório](images/dssmdo.png)

Em termos hierárquicos, o nó namespace contém "Seattle" e "Toronto". "Seattle" contém "Bellevue" e "Redmond". "Bellevue" e "Redmond" contêm um conjunto de contas de usuário. "Toronto" contém diretamente as contas de usuário sem nós organizacionais intermediários.

O componente de provedor de exemplo representa essa estrutura com apenas dois tipos de objeto Active Directory: um objeto de contêiner e um objeto folha. "Seattle", "Toronto", "Bellevue" e "Redmond" são objetos de contêiner e cada conta de usuário é um objeto folha.

O componente de provedor de exemplo cria uma classe de esquema chamada "Organizational Unit" para um tipo de objeto de contêiner e uma classe de esquema chamada "user" para uma conta de usuário.

As propriedades de cada classe de esquema, seus métodos e as regras que regem as relações de confinamento desses objetos são definidas no [Gerenciamento de esquema](schema-management.md).

 

 




