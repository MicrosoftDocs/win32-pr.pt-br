---
title: Pontos de sincronização
description: Quando há suporte para conjuntos de propriedades no mesmo objeto que o IStorage, é importante estar ciente dos pontos de sincronização entre o armazenamento de base e o armazenamento de propriedades.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637257"
---
# <a name="synchronization-points"></a><span data-ttu-id="d4d9f-103">Pontos de sincronização</span><span class="sxs-lookup"><span data-stu-id="d4d9f-103">Synchronization Points</span></span>

<span data-ttu-id="d4d9f-104">Quando há suporte para conjuntos de propriedades no mesmo objeto que o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), é importante estar ciente dos pontos de sincronização entre o armazenamento de base e o armazenamento de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d4d9f-104">When property sets are supported on the same object as [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), it is important to be aware of synchronization points between the base storage and the property storage.</span></span>

<span data-ttu-id="d4d9f-105">O armazenamento do conjunto de propriedades mantém o fluxo do conjunto de propriedades em um buffer interno até que o buffer seja confirmado por meio do método [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) .</span><span class="sxs-lookup"><span data-stu-id="d4d9f-105">The property set storage holds the property set stream in an internal buffer until that buffer is committed through the [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) method.</span></span> <span data-ttu-id="d4d9f-106">Isso é verdadeiro se [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) foi aberto no modo transacionado ou em modo direto.</span><span class="sxs-lookup"><span data-stu-id="d4d9f-106">This is true whether [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) was opened in transacted mode or in direct mode.</span></span>

 

 




