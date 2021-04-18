---
description: A propriedade ProductLanguage deve ser atualizada para o identificador de idioma numérico (LANGid) para o novo idioma.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Atualizando Propriedades ProductLanguage e ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758756"
---
# <a name="updating-productlanguage-and-productcode-properties"></a><span data-ttu-id="df39a-103">Atualizando Propriedades ProductLanguage e ProductCode</span><span class="sxs-lookup"><span data-stu-id="df39a-103">Updating ProductLanguage and ProductCode Properties</span></span>

<span data-ttu-id="df39a-104">A propriedade [**ProductLanguage**](productlanguage.md) deve ser atualizada para o identificador de idioma numérico (LangID) para o novo idioma.</span><span class="sxs-lookup"><span data-stu-id="df39a-104">The [**ProductLanguage**](productlanguage.md) property must be updated to the numeric language identifier (LANGID) for the new language.</span></span> <span data-ttu-id="df39a-105">No caso do exemplo de localização, o valor da propriedade **ProductLanguage** deve ser alterado do LangID para inglês (1033) para o LANGID para francês (1036) na tabela de [Propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="df39a-105">In the case of the localization example, the value of the **ProductLanguage** property must be changed from the LANGID for English (1033) to the LANGID for French (1036) in the [Property table](property-table.md).</span></span>

<span data-ttu-id="df39a-106">O valor da propriedade [**ProductCode**](productcode.md) na tabela de [Propriedades](property-table.md) deve ser alterado para um valor novo e exclusivo ao localizar um banco de dados, pois um produto localizado é considerado um produto diferente.</span><span class="sxs-lookup"><span data-stu-id="df39a-106">The value of the [**ProductCode**](productcode.md) property in the [Property table](property-table.md) must be changed to a new, unique value when localizing a database because a localized product is considered a different product.</span></span> <span data-ttu-id="df39a-107">Por exemplo, as versões em alemão e em inglês de um aplicativo são consideradas dois produtos diferentes e devem ter códigos de produto diferentes.</span><span class="sxs-lookup"><span data-stu-id="df39a-107">For example, the German and English versions of an application are considered two different products and must have different product codes.</span></span> <span data-ttu-id="df39a-108">Consulte [códigos de produto](product-codes.md).</span><span class="sxs-lookup"><span data-stu-id="df39a-108">See [Product Codes](product-codes.md).</span></span>

<span data-ttu-id="df39a-109">Use o editor de tabela de banco de dados para atualizar os valores das propriedades ProductCode e ProductLanguage na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="df39a-109">Use your database table editor to update the values of the ProductCode and ProductLanguage properties in the Property table.</span></span> <span data-ttu-id="df39a-110">Não reutilize o GUID mostrado se você copiar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="df39a-110">Do not reuse the GUID shown if you copy this example.</span></span>

[<span data-ttu-id="df39a-111">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="df39a-111">Property Table</span></span>](property-table.md)



| <span data-ttu-id="df39a-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="df39a-112">Property</span></span>                                   | <span data-ttu-id="df39a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="df39a-113">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="df39a-114">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="df39a-114">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="df39a-115">{EE389960-E426-4EEA-B669-AD8129249881}</span><span class="sxs-lookup"><span data-stu-id="df39a-115">{EE389960-E426-4EEA-B669-AD8129249881}</span></span> |
| [<span data-ttu-id="df39a-116">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="df39a-116">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="df39a-117">1036</span><span class="sxs-lookup"><span data-stu-id="df39a-117">1036</span></span>                                   |



 

[<span data-ttu-id="df39a-118">Continuar</span><span class="sxs-lookup"><span data-stu-id="df39a-118">Continue</span></span>](updating-a-summary-information-stream.md)

 

 



