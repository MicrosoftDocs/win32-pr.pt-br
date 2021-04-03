---
title: Controle de acesso e operações de gravação
description: As modificações de propriedade falharão se o chamador não tiver direitos suficientes.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- Controle de acesso e operações de gravador AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823623"
---
# <a name="access-control-and-write-operations"></a><span data-ttu-id="aa411-104">Controle de acesso e operações de gravação</span><span class="sxs-lookup"><span data-stu-id="aa411-104">Access Control and Write Operations</span></span>

<span data-ttu-id="aa411-105">As modificações de propriedade falharão se o chamador não tiver direitos suficientes.</span><span class="sxs-lookup"><span data-stu-id="aa411-105">Property modifications fail if the caller does not have sufficient rights.</span></span> <span data-ttu-id="aa411-106">Para operações de gravação que modificam o lote para várias propriedades, toda a operação falhará se o chamador não tiver os direitos necessários para uma única das propriedades modificadas.</span><span class="sxs-lookup"><span data-stu-id="aa411-106">For write operations that batch modifications to multiple properties, the entire operation fails if the caller does not have the necessary rights to a single one of the modified properties.</span></span> <span data-ttu-id="aa411-107">Por exemplo, você pode fazer várias chamadas [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) para definir várias propriedades em um objeto.</span><span class="sxs-lookup"><span data-stu-id="aa411-107">For example, you can make multiple [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) calls to set multiple properties on an object.</span></span> <span data-ttu-id="aa411-108">No entanto, quando você chamar [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para gravar os novos dados do cache local no diretório, o **setinfo** falhará se o chamador não tiver acesso de gravação a todas as propriedades modificadas.</span><span class="sxs-lookup"><span data-stu-id="aa411-108">However, when you call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to write the new data from the local cache to the directory, **SetInfo** will fail if the caller does not have write access to all the modified properties.</span></span> <span data-ttu-id="aa411-109">Da mesma forma, o método [**IDirectoryObject:: Setobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) falha ao definir qualquer propriedade se o chamador não tiver acesso a todas as propriedades que estão sendo definidas.</span><span class="sxs-lookup"><span data-stu-id="aa411-109">Similarly, the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) method fails to set any properties if the caller does not have access to all the properties being set.</span></span> <span data-ttu-id="aa411-110">Portanto, você deve enviar várias operações de modificação em lote apenas se souber que todas as modificações terão sucesso.</span><span class="sxs-lookup"><span data-stu-id="aa411-110">So you should batch multiple modify operations only if you know that all modifications will succeed.</span></span> <span data-ttu-id="aa411-111">Para determinar os atributos de um objeto de diretório que o chamador tem a capacidade de modificar, leia o atributo **allowedAttributesEffective** do objeto.</span><span class="sxs-lookup"><span data-stu-id="aa411-111">To determine the attributes of a directory object that the caller has the ability to modify, read the object's **allowedAttributesEffective** attribute.</span></span>

<span data-ttu-id="aa411-112">Se o chamador não tiver direitos suficientes para modificar uma propriedade, os códigos de retorno a seguir poderão ser retornados:</span><span class="sxs-lookup"><span data-stu-id="aa411-112">If the caller does not have sufficient rights to modify a property, the following return codes may be returned:</span></span>

<span data-ttu-id="aa411-113">Propriedade \_ de \_ ADS \_ não \_ definida e \_ \_ Propriedade ADS \_ não \_ modificada</span><span class="sxs-lookup"><span data-stu-id="aa411-113">E\_ADS\_PROPERTY\_NOT\_SET E\_ADS\_PROPERTY\_NOT\_MODIFIED</span></span>

 

 