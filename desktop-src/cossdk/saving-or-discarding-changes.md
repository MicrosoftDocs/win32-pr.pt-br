---
description: Salvando ou descartando alterações
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Salvando ou descartando alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826254"
---
# <a name="saving-or-discarding-changes"></a><span data-ttu-id="27dd3-103">Salvando ou descartando alterações</span><span class="sxs-lookup"><span data-stu-id="27dd3-103">Saving or Discarding Changes</span></span>

<span data-ttu-id="27dd3-104">Quando você define propriedades em um item, nenhuma alteração é realmente registrada no catálogo COM+ até que você salve explicitamente as alterações.</span><span class="sxs-lookup"><span data-stu-id="27dd3-104">When you set properties on an item, no changes are actually recorded to the COM+ catalog until you explicitly save changes.</span></span> <span data-ttu-id="27dd3-105">Você faz isso usando o método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para a coleção que contém o item.</span><span class="sxs-lookup"><span data-stu-id="27dd3-105">You do this using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object for the collection containing the item.</span></span>

<span data-ttu-id="27dd3-106">Se você quiser descartar as alterações que ainda não foram confirmadas, você pode chamar o método [**populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="27dd3-106">If you want to discard changes that have not yet been committed, you can call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="27dd3-107">Isso lê todos os dados persistentes do catálogo COM+ para todos os itens na coleção, excluindo efetivamente todas as alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="27dd3-107">This reads in all persistent data from the COM+ catalog for all items in the collection, effectively deleting any pending changes.</span></span>

<span data-ttu-id="27dd3-108">Quando você usa [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), todas as inconsistências nas configurações de propriedade escolhidas resultam em um erro e o **SaveChanges** não grava o objeto que retornou o erro.</span><span class="sxs-lookup"><span data-stu-id="27dd3-108">When you use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), any inconsistencies in property settings that you have chosen result in an error, and **SaveChanges** fails to write the object that returned the error.</span></span> <span data-ttu-id="27dd3-109">Todas as propriedades em um determinado item são gravadas ou não são gravadas como um todo.</span><span class="sxs-lookup"><span data-stu-id="27dd3-109">All properties on a given item either are written or fail to be written as a whole.</span></span>

<span data-ttu-id="27dd3-110">No entanto, quando ocorrem erros de gravação, eles podem não ser devido a configurações incompatíveis; alguma outra falha pode ter ocorrido.</span><span class="sxs-lookup"><span data-stu-id="27dd3-110">However, when write errors occur, they might not be due to incompatible settings; some other failure might have occurred.</span></span> <span data-ttu-id="27dd3-111">Você precisa inspecionar os detalhes da falha para ter certeza.</span><span class="sxs-lookup"><span data-stu-id="27dd3-111">You need to inspect the details of the failure to be certain.</span></span> <span data-ttu-id="27dd3-112">Para obter mais informações, consulte [lidando com erros de administração com+](handling-com--administration-errors.md) e [interdependências entre Propriedades](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="27dd3-112">For more information, see [Handling COM+ Administration Errors](handling-com--administration-errors.md) and [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="27dd3-113">Como regra geral, quanto mais alterações você tentar salvar ao mesmo tempo, particularmente as alterações em vários objetos, mais provavelmente você receberá um erro e mais difícil será rastrear.</span><span class="sxs-lookup"><span data-stu-id="27dd3-113">As a general rule, the more changes you attempt to save at once, particularly changes to multiple objects, the more likely you are to get an error and the more difficult it is to track down.</span></span>

<span data-ttu-id="27dd3-114">Além disso, entre as chamadas para [**popular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), você não tem um bloqueio nos itens da coleção; a contenção é possível.</span><span class="sxs-lookup"><span data-stu-id="27dd3-114">Additionally, between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), you do not have a lock on the items in the collection; contention is possible.</span></span> <span data-ttu-id="27dd3-115">Para obter mais detalhes, consulte [obtendo e Configurando Propriedades](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="27dd3-115">For more details, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="27dd3-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27dd3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27dd3-117">Obtendo e definindo propriedades</span><span class="sxs-lookup"><span data-stu-id="27dd3-117">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="27dd3-118">Interdependências entre propriedades</span><span class="sxs-lookup"><span data-stu-id="27dd3-118">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="27dd3-119">Consultando as propriedades disponíveis</span><span class="sxs-lookup"><span data-stu-id="27dd3-119">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> </dl>

 

 



