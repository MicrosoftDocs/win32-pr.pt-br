---
title: Localizando objetos por classe
description: As consultas de pesquisa típicas para uma classe de objeto específica.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Localizando objetos por AD de classe
- Active Directory, usando, pesquisando, por classe
- ANÚNCIO de objeto, pesquisando por classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756494"
---
# <a name="finding-objects-by-class"></a><span data-ttu-id="8ba9e-106">Localizando objetos por classe</span><span class="sxs-lookup"><span data-stu-id="8ba9e-106">Finding Objects by Class</span></span>

<span data-ttu-id="8ba9e-107">As consultas de pesquisa típicas para uma classe de objeto específica.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-107">A typical search queries for a specific object class.</span></span> <span data-ttu-id="8ba9e-108">O exemplo de código a seguir pesquisa computadores com o local em Compilando 7N.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-108">The following code example searches for computers with location in Building 7N.</span></span>


```C++
(&(objectCategory=computer)(location=Building 7N))
```



<span data-ttu-id="8ba9e-109">Considere por que o **objectClass** não é usado.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-109">Consider why **objectClass** is not used.</span></span> <span data-ttu-id="8ba9e-110">Não use **objectClass** sem outra comparação que contenha um atributo indexado.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-110">Do not use **objectClass** without another comparison that contains an indexed attribute.</span></span> <span data-ttu-id="8ba9e-111">Atributos de índice podem aumentar a eficiência de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-111">Index attributes can increase the efficiency of a query.</span></span> <span data-ttu-id="8ba9e-112">O atributo **objectClass** tem valores múltiplos e não indexados.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-112">The **objectClass** attribute is multi-valued and not indexed.</span></span> <span data-ttu-id="8ba9e-113">Para especificar o tipo ou a classe de um objeto, use **objectCategory**.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-113">To specify the type or class of an object, use **objectCategory**.</span></span>

<span data-ttu-id="8ba9e-114">Menos eficiente:</span><span class="sxs-lookup"><span data-stu-id="8ba9e-114">Less efficient:</span></span>


```C++
(objectClass=computer)
```



<span data-ttu-id="8ba9e-115">Mais eficiente:</span><span class="sxs-lookup"><span data-stu-id="8ba9e-115">More Efficient:</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="8ba9e-116">Lembre-se de que há alguns casos em que uma combinação de **objectClass** e **objectCategory** deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-116">Be aware that there are some cases where a combination of **objectClass** and **objectCategory** must be used.</span></span> <span data-ttu-id="8ba9e-117">A classe de usuário e a classe de contato devem ser especificadas da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-117">The user class and contact class should be specified as follows.</span></span>


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



<span data-ttu-id="8ba9e-118">Lembre-se de que você pode pesquisar por usuários e contatos com o seguinte.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-118">Be aware that you could search for both users and contacts with the following.</span></span>


```C++
(objectCategory=person)
```



 

 




