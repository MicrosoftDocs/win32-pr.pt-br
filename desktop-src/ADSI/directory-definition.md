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
# <a name="directory-definition"></a><span data-ttu-id="0c4e0-103">Definição de diretório</span><span class="sxs-lookup"><span data-stu-id="0c4e0-103">Directory Definition</span></span>

<span data-ttu-id="0c4e0-104">O componente de provedor de exemplo usa um design de diretório relativamente simples para esclarecer a relação entre componentes e mostrar os requisitos mínimos necessários para ser um provedor ADSI.</span><span class="sxs-lookup"><span data-stu-id="0c4e0-104">The example provider component uses a relatively simple directory design to clarify the relationship between components and to show the minimum requirements necessary to be an ADSI provider.</span></span>

<span data-ttu-id="0c4e0-105">O "diretório" para o componente de provedor de exemplo consiste em dois nós raiz: "Seattle" e "Toronto".</span><span class="sxs-lookup"><span data-stu-id="0c4e0-105">The "directory" for the example provider component consists of two root nodes: "Seattle" and "Toronto".</span></span> <span data-ttu-id="0c4e0-106">Seattle contém mais dois subníveis, "Bellevue" e "Redmond".</span><span class="sxs-lookup"><span data-stu-id="0c4e0-106">Seattle contains two more sublevels, "Bellevue" and "Redmond".</span></span> <span data-ttu-id="0c4e0-107">Cada uma dessas entradas contém várias contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="0c4e0-107">Each of these entries contains several user accounts.</span></span> <span data-ttu-id="0c4e0-108">A entrada "Toronto" não tem mais subníveis, mas contém diretamente várias contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="0c4e0-108">The "Toronto" entry has no further sublevels, but directly contains several user accounts.</span></span> <span data-ttu-id="0c4e0-109">A figura a seguir mostra esses dois nós raiz conectados a uma rede.</span><span class="sxs-lookup"><span data-stu-id="0c4e0-109">The following figure shows these two root nodes connected to a network.</span></span>

![definição de diretório](images/dssmdo.png)

<span data-ttu-id="0c4e0-111">Em termos hierárquicos, o nó namespace contém "Seattle" e "Toronto".</span><span class="sxs-lookup"><span data-stu-id="0c4e0-111">In hierarchical terms, the Namespace node contains "Seattle" and "Toronto".</span></span> <span data-ttu-id="0c4e0-112">"Seattle" contém "Bellevue" e "Redmond".</span><span class="sxs-lookup"><span data-stu-id="0c4e0-112">"Seattle" contains "Bellevue" and "Redmond".</span></span> <span data-ttu-id="0c4e0-113">"Bellevue" e "Redmond" contêm um conjunto de contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="0c4e0-113">"Bellevue" and "Redmond" each contain a set of user accounts.</span></span> <span data-ttu-id="0c4e0-114">"Toronto" contém diretamente as contas de usuário sem nós organizacionais intermediários.</span><span class="sxs-lookup"><span data-stu-id="0c4e0-114">"Toronto" directly contains the user accounts with no intermediate organizational nodes.</span></span>

<span data-ttu-id="0c4e0-115">O componente de provedor de exemplo representa essa estrutura com apenas dois tipos de objeto Active Directory: um objeto de contêiner e um objeto folha.</span><span class="sxs-lookup"><span data-stu-id="0c4e0-115">The example provider component represents this structure with only two Active Directory object types: a container object and a leaf object.</span></span> <span data-ttu-id="0c4e0-116">"Seattle", "Toronto", "Bellevue" e "Redmond" são objetos de contêiner e cada conta de usuário é um objeto folha.</span><span class="sxs-lookup"><span data-stu-id="0c4e0-116">"Seattle", "Toronto", "Bellevue", and "Redmond" are container objects and each user account is a leaf object.</span></span>

<span data-ttu-id="0c4e0-117">O componente de provedor de exemplo cria uma classe de esquema chamada "Organizational Unit" para um tipo de objeto de contêiner e uma classe de esquema chamada "user" para uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="0c4e0-117">The example provider component creates a schema class called "Organizational Unit" for a container object type and a schema class called "User" for a user account.</span></span>

<span data-ttu-id="0c4e0-118">As propriedades de cada classe de esquema, seus métodos e as regras que regem as relações de confinamento desses objetos são definidas no [Gerenciamento de esquema](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="0c4e0-118">The properties for each schema class, their methods, and the rules that govern the containment relationships for these objects are all defined in [Schema Management](schema-management.md).</span></span>

 

 




