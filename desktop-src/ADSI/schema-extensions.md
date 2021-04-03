---
title: Extensões de esquema
description: A arquitetura do esquema ADSI fornece que novas classes de esquema podem ser adicionadas ao contêiner de classes de esquema e novas propriedades a um objeto de classe de esquema existente em tempo de execução.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084001"
---
# <a name="schema-extensions"></a><span data-ttu-id="5ca4d-103">Extensões de esquema</span><span class="sxs-lookup"><span data-stu-id="5ca4d-103">Schema Extensions</span></span>

<span data-ttu-id="5ca4d-104">A arquitetura do esquema ADSI fornece que novas classes de esquema podem ser adicionadas ao contêiner de classes de esquema e novas propriedades a um objeto de classe de esquema existente em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5ca4d-104">The architecture of the ADSI schema provides that new schema classes can be added to the schema class container and new properties to an existing schema class object at run time.</span></span> <span data-ttu-id="5ca4d-105">A última capacidade não requer nenhum código novo.</span><span class="sxs-lookup"><span data-stu-id="5ca4d-105">The latter ability requires no new code.</span></span> <span data-ttu-id="5ca4d-106">Esse é um recurso importante para namespaces que permitem serviços de diretório extensível.</span><span class="sxs-lookup"><span data-stu-id="5ca4d-106">This is an important feature for namespaces that allow extensible directory services.</span></span> <span data-ttu-id="5ca4d-107">O componente do provedor deve permitir essa extensibilidade e saber onde acessar e armazenar a instância de classe e os valores de suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5ca4d-107">The provider component must allow for this extensibility and know where to access and store the class instance and the values of its properties.</span></span> <span data-ttu-id="5ca4d-108">Em um serviço de diretório extensível típico, essas informações são armazenadas no banco de dados do serviço de diretório da mesma maneira que qualquer outra classe de esquema e definições de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5ca4d-108">In a typical extensible directory service, this information is stored in the directory service database in the same manner as any other schema class and property definitions.</span></span>

> [!Note]  
> <span data-ttu-id="5ca4d-109">Na terminologia da interface COM, somente as propriedades podem ser adicionadas a uma classe de esquema existente, não a métodos.</span><span class="sxs-lookup"><span data-stu-id="5ca4d-109">In COM interface terminology, only properties can be added to an existing schema class, not methods.</span></span> <span data-ttu-id="5ca4d-110">Adicionar um novo método exigiria adicionar uma nova implementação desse método e, portanto, exigir código adicional.</span><span class="sxs-lookup"><span data-stu-id="5ca4d-110">Adding a new method would require adding a new implementation of that method and thus require additional code.</span></span>

 

<span data-ttu-id="5ca4d-111">Para obter um exemplo de um esquema de provedor específico, consulte [Gerenciamento de esquema](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="5ca4d-111">For an example of a specific provider schema, see [Schema Management](schema-management.md).</span></span>

 

 




