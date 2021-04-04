---
description: Um objeto é uma estrutura de dados que representa um recurso do sistema, como um arquivo, um thread ou uma imagem gráfica.
ms.assetid: 26aaad09-c1e1-46e8-9cd3-7d795a10d900
title: Identificadores e objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b5a35d55571a01f2f186f4e756401582474949f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836963"
---
# <a name="handles-and-objects"></a><span data-ttu-id="03b20-103">Identificadores e objetos</span><span class="sxs-lookup"><span data-stu-id="03b20-103">Handles and Objects</span></span>

<span data-ttu-id="03b20-104">Um *objeto* é uma estrutura de dados que representa um recurso do sistema, como um arquivo, um thread ou uma imagem gráfica.</span><span class="sxs-lookup"><span data-stu-id="03b20-104">An *object* is a data structure that represents a system resource, such as a file, thread, or graphic image.</span></span> <span data-ttu-id="03b20-105">Um aplicativo não pode acessar diretamente os dados do objeto ou o recurso do sistema que um objeto representa.</span><span class="sxs-lookup"><span data-stu-id="03b20-105">An application cannot directly access object data or the system resource that an object represents.</span></span> <span data-ttu-id="03b20-106">Em vez disso, um aplicativo deve obter um *identificador* de objeto, que pode ser usado para examinar ou modificar o recurso do sistema.</span><span class="sxs-lookup"><span data-stu-id="03b20-106">Instead, an application must obtain an object *handle*, which it can use to examine or modify the system resource.</span></span> <span data-ttu-id="03b20-107">Cada identificador tem uma entrada em uma tabela mantida internamente.</span><span class="sxs-lookup"><span data-stu-id="03b20-107">Each handle has an entry in an internally maintained table.</span></span> <span data-ttu-id="03b20-108">Essas entradas contêm os endereços dos recursos e os meios para identificar o tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="03b20-108">These entries contain the addresses of the resources and the means to identify the resource type.</span></span>

-   [<span data-ttu-id="03b20-109">Sobre identificadores e objetos</span><span class="sxs-lookup"><span data-stu-id="03b20-109">About Handles and Objects</span></span>](about-handles-and-objects.md)
-   [<span data-ttu-id="03b20-110">Categorias de objeto</span><span class="sxs-lookup"><span data-stu-id="03b20-110">Object Categories</span></span>](object-categories.md)
-   [<span data-ttu-id="03b20-111">Identificador e referência de objeto</span><span class="sxs-lookup"><span data-stu-id="03b20-111">Handle and Object Reference</span></span>](handle-and-object-reference.md)

 

 



