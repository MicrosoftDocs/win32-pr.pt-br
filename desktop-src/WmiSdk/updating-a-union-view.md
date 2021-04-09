---
description: Você pode atualizar os valores das propriedades não chave de instâncias de classe de exibição Union. As alterações feitas na instância da classe de exibição serão propagadas de volta para as instâncias de classe de origem que formam a classe de exibição Union.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Atualizando uma exibição Union
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091276"
---
# <a name="updating-a-union-view"></a><span data-ttu-id="d00b2-104">Atualizando uma exibição Union</span><span class="sxs-lookup"><span data-stu-id="d00b2-104">Updating a Union View</span></span>

<span data-ttu-id="d00b2-105">Você pode atualizar os valores das propriedades não chave de instâncias de classe de exibição Union.</span><span class="sxs-lookup"><span data-stu-id="d00b2-105">You can update the values of nonkey properties of union view class instances.</span></span> <span data-ttu-id="d00b2-106">As alterações feitas na instância da classe de exibição serão propagadas de volta para as instâncias de classe de origem que formam a classe de exibição Union.</span><span class="sxs-lookup"><span data-stu-id="d00b2-106">The changes you make to the view class instance will be propagated back to the source class instances that form the union view class.</span></span>

<span data-ttu-id="d00b2-107">As seguintes restrições se aplicam a alterações para exibir instâncias de classe:</span><span class="sxs-lookup"><span data-stu-id="d00b2-107">The following restrictions apply to changes to view class instances:</span></span>

-   <span data-ttu-id="d00b2-108">Você não pode criar novas instâncias de classes de exibição.</span><span class="sxs-lookup"><span data-stu-id="d00b2-108">You cannot create new instances of view classes.</span></span>
-   <span data-ttu-id="d00b2-109">Somente as classes Union dão suporte a atualizações; as exibições de junção e Associação criam instâncias de exibição somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d00b2-109">Only union classes support updates; join and association views create read-only view instances.</span></span>
-   <span data-ttu-id="d00b2-110">O sucesso de uma atualização depende se uma instância de origem é atualizável.</span><span class="sxs-lookup"><span data-stu-id="d00b2-110">Success of an update depends on whether a source instance is updateable.</span></span> <span data-ttu-id="d00b2-111">Se uma propriedade de exibição de instância for mapeada para uma propriedade somente leitura de uma instância de origem, as tentativas de modificar a propriedade de exibição falharão.</span><span class="sxs-lookup"><span data-stu-id="d00b2-111">If a view instance property maps to a read-only property of a source instance, attempts to modify the view property fail.</span></span>

 

 



