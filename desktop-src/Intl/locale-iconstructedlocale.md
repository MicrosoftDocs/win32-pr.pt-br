---
description: '\_Descrição da constante ICONSTRUCTEDLOCALE de localidade'
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/30/2021
ms.locfileid: "105995141"
---
# <a name="locale_iconstructedlocale"></a><span data-ttu-id="bae5e-103">ICONSTRUCTEDLOCALE de localidade \_</span><span class="sxs-lookup"><span data-stu-id="bae5e-103">LOCALE\_ICONSTRUCTEDLOCALE</span></span>

<span data-ttu-id="bae5e-104">Identificador a ser solicitado se a localidade for uma localidade "construída".</span><span class="sxs-lookup"><span data-stu-id="bae5e-104">Identifier to request if the locale is a "constructed" locale.</span></span> <span data-ttu-id="bae5e-105">O uso desse LCTYPE não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="bae5e-105">Use of this LCTYPE is discouraged.</span></span>

<span data-ttu-id="bae5e-106">Isso identifica uma localidade para a qual o Windows não tem informações completas e tem de "construir" informações em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="bae5e-106">This identifies a locale for which Windows many not have complete information and has to "construct" information at runtime.</span></span> <span data-ttu-id="bae5e-107">Normalmente, as informações fornecidas pelo LOCALE_ICONSTRUCTEDLOCALE são de uso limitado, pois o Windows fornecerá tantos dados quantos estiverem disponíveis para cada localidade.</span><span class="sxs-lookup"><span data-stu-id="bae5e-107">Typically the information provided by LOCALE_ICONSTRUCTEDLOCALE is of limited use as Windows will provide as much data as is available for every locale.</span></span> <span data-ttu-id="bae5e-108">Portanto, o uso desse LCTYPE não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="bae5e-108">Therefore, use of this LCTYPE is discouraged.</span></span>


| <span data-ttu-id="bae5e-109">Valor</span><span class="sxs-lookup"><span data-stu-id="bae5e-109">Value</span></span> | <span data-ttu-id="bae5e-110">Significado</span><span class="sxs-lookup"><span data-stu-id="bae5e-110">Meaning</span></span>                 |
|-------|-------------------------|
| <span data-ttu-id="bae5e-111">0</span><span class="sxs-lookup"><span data-stu-id="bae5e-111">0</span></span>     | <span data-ttu-id="bae5e-112">Não construído</span><span class="sxs-lookup"><span data-stu-id="bae5e-112">Not constructed</span></span>         |
| <span data-ttu-id="bae5e-113">1</span><span class="sxs-lookup"><span data-stu-id="bae5e-113">1</span></span>     | <span data-ttu-id="bae5e-114">É uma localidade construída</span><span class="sxs-lookup"><span data-stu-id="bae5e-114">Is a constructed locale</span></span> |


<span data-ttu-id="bae5e-115">Um exemplo seria uma solicitação para "de-US" ou para o alemão na Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="bae5e-115">An example would be a request for "de-US", or German in the United States.</span></span> <span data-ttu-id="bae5e-116">O NLS usará os dados do idioma alemão que ele pode encontrar e os Estados Unidos dados de região que ele pode encontrar.</span><span class="sxs-lookup"><span data-stu-id="bae5e-116">NLS will use the German language data that it can find and the United States region data that it can find.</span></span> 

<span data-ttu-id="bae5e-117">Isso pode não ser perfeito, como, por exemplo, o sistema provavelmente não terá informações sobre o nome de Estados Unidos em alemão.</span><span class="sxs-lookup"><span data-stu-id="bae5e-117">This may not be perfect as, for example, the system will likely not have information about the name of United States in German.</span></span> <span data-ttu-id="bae5e-118">No entanto, se o aplicativo ou o usuário desejar um contexto "de-US", os dados retornados serão os melhores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bae5e-118">However, if the application or user desires a "de-US" context, then the returned data is the best available.</span></span> 

<span data-ttu-id="bae5e-119">Os aplicativos que usam LOCALE_ICONSTRUCTEDLOCALE para rejeitar as localidades e fazer fallback para uma localidade diferente normalmente acabam com uma experiência pior, como a aterrissagem em de-DE-ou en-US neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="bae5e-119">Apps that use LOCALE_ICONSTRUCTEDLOCALE to reject locales and fall back to a different locale typically end up with a worse experience, such as landing on de-DE or en-US in this example.</span></span> <span data-ttu-id="bae5e-120">Nenhuma delas está perto da solicitação original para o idioma alemão com uma região Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="bae5e-120">Neither of those are close to the original request for German language with a United States region.</span></span>

