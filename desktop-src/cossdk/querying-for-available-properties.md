---
description: Consultando as propriedades disponíveis
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Consultando as propriedades disponíveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089497"
---
# <a name="querying-for-available-properties"></a><span data-ttu-id="c0a23-103">Consultando as propriedades disponíveis</span><span class="sxs-lookup"><span data-stu-id="c0a23-103">Querying for Available Properties</span></span>

<span data-ttu-id="c0a23-104">Se você estiver escrevendo uma ferramenta de administração de finalidade geral, provavelmente precisará escrever rotinas para definir propriedades de forma completa.</span><span class="sxs-lookup"><span data-stu-id="c0a23-104">If you are writing a general-purpose administration tool, you most likely will need to write routines for setting properties in full generality.</span></span> <span data-ttu-id="c0a23-105">Para dar suporte a isso, há uma instalação que permite que você consulte dinamicamente as propriedades que estão disponíveis para os itens em qualquer coleção específica.</span><span class="sxs-lookup"><span data-stu-id="c0a23-105">To support this, there is a facility that enables you to dynamically query for the properties that are available for the items in any given collection.</span></span>

<span data-ttu-id="c0a23-106">A coleção [**PropertyInfo**](propertyinfo.md) está disponível em qualquer coleção que você esteja mantendo.</span><span class="sxs-lookup"><span data-stu-id="c0a23-106">The [**PropertyInfo**](propertyinfo.md) collection is available from any collection that you might be holding.</span></span> <span data-ttu-id="c0a23-107">A coleção **PropertyInfo** contém um item para cada propriedade disponível.</span><span class="sxs-lookup"><span data-stu-id="c0a23-107">The **PropertyInfo** collection contains an item for each available property.</span></span> <span data-ttu-id="c0a23-108">Você pode enumerar esses itens para determinar se uma determinada propriedade está disponível.</span><span class="sxs-lookup"><span data-stu-id="c0a23-108">You can enumerate through these items to determine whether a given property is available.</span></span>

<span data-ttu-id="c0a23-109">Você pode obter a coleção [**PropertyInfo**](propertyinfo.md) de qualquer coleção que você esteja mantendo usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , deixando o segundo parâmetro em branco, em que você normalmente especificaria a propriedade de chave de um item pai.</span><span class="sxs-lookup"><span data-stu-id="c0a23-109">You can get the [**PropertyInfo**](propertyinfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0a23-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0a23-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0a23-111">Obtendo e definindo propriedades</span><span class="sxs-lookup"><span data-stu-id="c0a23-111">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="c0a23-112">Interdependências entre propriedades</span><span class="sxs-lookup"><span data-stu-id="c0a23-112">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="c0a23-113">Salvando ou descartando alterações</span><span class="sxs-lookup"><span data-stu-id="c0a23-113">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



