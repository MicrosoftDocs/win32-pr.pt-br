---
title: Atributos indexados (AD DS)
description: Os atributos podem ser indexados. A indexação de um atributo pode melhorar o desempenho de consultas para esse atributo.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- AD de atributos indexados
- Atributos AD, indexado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105751016"
---
# <a name="indexed-attributes-ad-ds"></a><span data-ttu-id="bfd97-106">Atributos indexados (AD DS)</span><span class="sxs-lookup"><span data-stu-id="bfd97-106">Indexed Attributes (AD DS)</span></span>

<span data-ttu-id="bfd97-107">Os atributos podem ser indexados.</span><span class="sxs-lookup"><span data-stu-id="bfd97-107">Attributes may be indexed.</span></span> <span data-ttu-id="bfd97-108">A indexação de um atributo pode melhorar o desempenho de consultas para esse atributo.</span><span class="sxs-lookup"><span data-stu-id="bfd97-108">Indexing an attribute can improve the performance of queries for that attribute.</span></span>

<span data-ttu-id="bfd97-109">Os atributos são indexados quando o atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) na definição de esquema do atributo tem o bit menos significativo definido como 1.</span><span class="sxs-lookup"><span data-stu-id="bfd97-109">An attributes is indexed when the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute in the attribute's schema definition has the least significant bit set to 1.</span></span> <span data-ttu-id="bfd97-110">Definir o bit menos significativo da definição de esquema de atributo **searchFlags** como 1 criará um índice dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="bfd97-110">Setting the least significant bit of the **searchFlags** attribute schema definition to 1 will dynamically build an index.</span></span> <span data-ttu-id="bfd97-111">Definir o bit menos significativo da definição de esquema de atributo **searchFlags** como 0 fará com que o índice do atributo seja removido.</span><span class="sxs-lookup"><span data-stu-id="bfd97-111">Setting the least significant bit of the **searchFlags** attribute schema definition to 0 will cause the index for the attribute to be removed.</span></span> <span data-ttu-id="bfd97-112">O índice será criado automaticamente por um thread em segundo plano no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="bfd97-112">The index will be built automatically by a background thread on the domain controller.</span></span>

<span data-ttu-id="bfd97-113">O ideal é que os atributos indexados tenham um valor único com valores altamente exclusivos distribuídos uniformemente no conjunto de instâncias.</span><span class="sxs-lookup"><span data-stu-id="bfd97-113">Ideally, indexed attributes should be single valued with highly unique values evenly distributed across the set of instances.</span></span> <span data-ttu-id="bfd97-114">Quanto menos únicos forem os valores de um atributo, menos efetivo será o índice.</span><span class="sxs-lookup"><span data-stu-id="bfd97-114">The less unique the values of an attribute are, the less effective the index will be.</span></span>

<span data-ttu-id="bfd97-115">Os atributos com valores múltiplos também podem ser indexados, mas o custo para criar o índice para um atributo com vários valores é maior em termos de armazenamento, atualização e tempo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="bfd97-115">Multi-valued attributes can also be indexed, but the cost to build the index for a multi-valued attribute is larger in terms of storage, update, and search time.</span></span> <span data-ttu-id="bfd97-116">O requisito de exclusividade para uma propriedade de valores múltiplos é o mesmo que para uma propriedade de valor único; quanto mais exclusivo, os valores são mais eficazes para o índice.</span><span class="sxs-lookup"><span data-stu-id="bfd97-116">The uniqueness requirement for a multi-valued property is the same as that for a single-valued property—the more unique the values are the more effective the index.</span></span>

<span data-ttu-id="bfd97-117">Quanto mais atributos indexados uma classe tiver, mais tempo será necessário para criar novas instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="bfd97-117">The more indexed attributes a class has, the more time is required to create new instances of the class.</span></span>

<span data-ttu-id="bfd97-118">Os índices se aplicam a atributos, e não a classes.</span><span class="sxs-lookup"><span data-stu-id="bfd97-118">Indexes apply to attributes, not to classes.</span></span> <span data-ttu-id="bfd97-119">Ou seja, quando um atributo é marcado como indexado, todas as instâncias do atributo são adicionadas ao índice, não apenas às instâncias que são membros de uma classe específica.</span><span class="sxs-lookup"><span data-stu-id="bfd97-119">That is, when an attribute is marked as indexed, all instances of the attribute are added to the index, not just the instances that are members of a particular class.</span></span>

<span data-ttu-id="bfd97-120">Para verificar se um servidor está usando um índice para processar uma consulta, defina o valor do registro a seguir em um controlador de domínio como 4.</span><span class="sxs-lookup"><span data-stu-id="bfd97-120">To verify that a server is using an index to process a query, set the following registry value on a domain controller to 4.</span></span> <span data-ttu-id="bfd97-121">Em seguida, execute uma consulta nesse controlador de domínio e procure no log de eventos do diretório dados sobre os índices, se houver, usados para processar a consulta.</span><span class="sxs-lookup"><span data-stu-id="bfd97-121">Then perform a query on that domain controller and look in the directory event log for data about the indexes, if any, used to process the query.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

<span data-ttu-id="bfd97-122">Para obter mais informações sobre outros bits na propriedade [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) , consulte [características de atributos](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="bfd97-122">For more information about other bits in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) property, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

 

 