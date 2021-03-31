---
description: Usando dados de localidade persistente
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Usando dados de localidade persistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837418"
---
# <a name="using-persistent-locale-data"></a><span data-ttu-id="aed79-103">Usando dados de localidade persistente</span><span class="sxs-lookup"><span data-stu-id="aed79-103">Using Persistent Locale Data</span></span>

<span data-ttu-id="aed79-104">Um aplicativo globalizado geralmente mantém ou transmite dados, por exemplo, data e hora.</span><span class="sxs-lookup"><span data-stu-id="aed79-104">A globalized application often persists or transmits data, for example, time and date.</span></span> <span data-ttu-id="aed79-105">Ao decidir como seu aplicativo deve lidar com a persistência de dados, lembre-se de que não há garantia de que os dados sejam os mesmos do computador para o computador ou entre as execuções do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aed79-105">When deciding how your application should handle data persistence, remember that data is not guaranteed to be the same from computer to computer or between runs of the application.</span></span> <span data-ttu-id="aed79-106">Isso é verdadeiro para as [localidades](locales-and-languages.md) fornecidas com o Windows e as [localidades personalizadas](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="aed79-106">This is true for both [locales](locales-and-languages.md) that ship with Windows and [custom locales](custom-locales.md).</span></span>

<span data-ttu-id="aed79-107">O design do aplicativo deve levar em conta uma variedade de alterações de dados relacionadas à localidade que podem ocorrer.</span><span class="sxs-lookup"><span data-stu-id="aed79-107">Design of the application must take into account a variety of locale-related data changes that can occur.</span></span> <span data-ttu-id="aed79-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="aed79-108">For example:</span></span>

-   <span data-ttu-id="aed79-109">Os símbolos de moeda podem mudar conforme os países adotam o euro.</span><span class="sxs-lookup"><span data-stu-id="aed79-109">Currency symbols can change as countries adopt the Euro.</span></span>
-   <span data-ttu-id="aed79-110">As preferências regionais podem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="aed79-110">Regional preferences can change.</span></span> <span data-ttu-id="aed79-111">Por exemplo, o formato d/m/y pode mudar para o formato m/d/y de uma localidade específica.</span><span class="sxs-lookup"><span data-stu-id="aed79-111">For example, the format d/m/y might change to the format m/d/y for a particular locale.</span></span>
-   <span data-ttu-id="aed79-112">A ortografia dos nomes de dias pode mudar devido à reforms de ortografia.</span><span class="sxs-lookup"><span data-stu-id="aed79-112">The spelling of day names can change due to spelling reforms.</span></span> <span data-ttu-id="aed79-113">Além disso, a capitalização pode mudar para os nomes de mês ou dia.</span><span class="sxs-lookup"><span data-stu-id="aed79-113">Additionally, casing can change for month or day names.</span></span>

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a><span data-ttu-id="aed79-114">Usar formatos de Locale-Independent para armazenamento e troca de dados</span><span class="sxs-lookup"><span data-stu-id="aed79-114">Use Locale-Independent Formats for Storage and Data Interchange</span></span>

<span data-ttu-id="aed79-115">Um aplicativo que persiste dados deve usar formatos independentes de localidade para armazenamento e troca de dados.</span><span class="sxs-lookup"><span data-stu-id="aed79-115">An application that persists data should use locale-independent formats for storage and data interchange.</span></span> <span data-ttu-id="aed79-116">Os exemplos são formatos embutidos em código ou padrão; o nome da localidade de localidade invariável invariável e formatos de armazenamento binários. [ \_ \_ ](locale-name-constants.md)</span><span class="sxs-lookup"><span data-stu-id="aed79-116">Examples are hard-coded or standard formats; the invariant locale [LOCALE\_NAME\_INVARIANT](locale-name-constants.md); and binary storage formats.</span></span>

<span data-ttu-id="aed79-117">Se a classificação persistente de dados for necessária, o aplicativo deverá usar a função [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) .</span><span class="sxs-lookup"><span data-stu-id="aed79-117">If persistent sorting data is required, the application must use the [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) function.</span></span> <span data-ttu-id="aed79-118">Lembre-se de que um formato invariável não permanece invariável para [classificação](sorting.md), somente para dados de localidade e calendário.</span><span class="sxs-lookup"><span data-stu-id="aed79-118">Remember that an invariant format does not remain invariant for [sorting](sorting.md), only for locale and calendar data.</span></span>

## <a name="use-the-user-default-locale-for-data-presentation"></a><span data-ttu-id="aed79-119">Usar a localidade padrão do usuário para a apresentação de dados</span><span class="sxs-lookup"><span data-stu-id="aed79-119">Use the User Default Locale for Data Presentation</span></span>

<span data-ttu-id="aed79-120">Para apresentar dados persistentes, é melhor para o aplicativo reformatar os dados usando a localidade padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="aed79-120">To present persistent data, it is best for the application to reformat the data using the user default locale.</span></span> <span data-ttu-id="aed79-121">O uso dessa localidade permite substituições do usuário.</span><span class="sxs-lookup"><span data-stu-id="aed79-121">Use of this locale allows user overrides.</span></span> <span data-ttu-id="aed79-122">Para obter mais informações, consulte [local \_ user \_ Default](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="aed79-122">For more information, see [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aed79-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aed79-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aed79-124">Usando o suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="aed79-124">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="aed79-125">Localidades personalizadas</span><span class="sxs-lookup"><span data-stu-id="aed79-125">Custom Locales</span></span>](custom-locales.md)
</dt> <dt>

[<span data-ttu-id="aed79-126">Classificação</span><span class="sxs-lookup"><span data-stu-id="aed79-126">Sorting</span></span>](sorting.md)
</dt> </dl>

 

 



