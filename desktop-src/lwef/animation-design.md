---
title: Design de animação
description: Design de animação
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916153"
---
# <a name="animation-design"></a><span data-ttu-id="aa516-103">Design de animação</span><span class="sxs-lookup"><span data-stu-id="aa516-103">Animation Design</span></span>

<span data-ttu-id="aa516-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aa516-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

### <a name="image-design"></a><span data-ttu-id="aa516-105">Design de imagem</span><span class="sxs-lookup"><span data-stu-id="aa516-105">Image Design</span></span>

<span data-ttu-id="aa516-106">Use a paleta de Microsoft Office ao criar seus caracteres para minimizar possíveis problemas de realização de paleta.</span><span class="sxs-lookup"><span data-stu-id="aa516-106">Use the Microsoft Office Palette when designing your characters to minimize any potential palette realization issues.</span></span> <span data-ttu-id="aa516-107">Evite selecionar uma cor de transparência que seja semelhante às cores que você usa em seu documento.</span><span class="sxs-lookup"><span data-stu-id="aa516-107">Avoid selecting a transparency color that is similar to the colors that you use in your document.</span></span>

### <a name="sounds"></a><span data-ttu-id="aa516-108">Sons</span><span class="sxs-lookup"><span data-stu-id="aa516-108">Sounds</span></span>

<span data-ttu-id="aa516-109">O Microsoft Agent permite que você jogue sons em suas animações.</span><span class="sxs-lookup"><span data-stu-id="aa516-109">Microsoft Agent enables you to play sounds in your animations.</span></span> <span data-ttu-id="aa516-110">Recomendamos que você não inclua sons para suas animações **ociosas** .</span><span class="sxs-lookup"><span data-stu-id="aa516-110">We recommend you do not include sounds for your **Idle** animations.</span></span> <span data-ttu-id="aa516-111">Isso é assim, não haverá um atraso no meio da animação, se o Agent tiver que carregar a DLL de multimídia do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa516-111">This is so there won't be a delay in the middle of the animation, if Agent has to load the system multimedia DLL.</span></span>

### <a name="frame-size"></a><span data-ttu-id="aa516-112">Tamanho do quadro</span><span class="sxs-lookup"><span data-stu-id="aa516-112">Frame Size</span></span>

<span data-ttu-id="aa516-113">Os assistentes típicos do Office são 123 x 93 pixels.</span><span class="sxs-lookup"><span data-stu-id="aa516-113">Typical Office Assistants are 123 x 93 pixels.</span></span> <span data-ttu-id="aa516-114">Embora você possa criar caracteres de outros tamanhos, eles serão dimensionados para 123 x 93 na galeria do assistente.</span><span class="sxs-lookup"><span data-stu-id="aa516-114">While you can create characters of other sizes, they will be scaled to 123 x 93 in the Assistant Gallery.</span></span>

### <a name="frame-transition"></a><span data-ttu-id="aa516-115">Transição de quadros</span><span class="sxs-lookup"><span data-stu-id="aa516-115">Frame Transition</span></span>

<span data-ttu-id="aa516-116">Todas as animações, exceto para **adeus**, **saudação**, **Mostrar** e **ocultar** , devem começar e terminar com a animação RestPose.</span><span class="sxs-lookup"><span data-stu-id="aa516-116">All animations except for **Goodbye**, **Greeting**, **Show** and **Hide** should begin and end with the RestPose animation.</span></span> <span data-ttu-id="aa516-117">Microsoft Office não reproduz animações de **retorno** explícitas, portanto, você não deve defini-las.</span><span class="sxs-lookup"><span data-stu-id="aa516-117">Microsoft Office does not play explicit **Return** animations, so you should not define them.</span></span> <span data-ttu-id="aa516-118">Todas as animações também devem ter ramificações de saída.</span><span class="sxs-lookup"><span data-stu-id="aa516-118">All animations should also have Exit Branching.</span></span> <span data-ttu-id="aa516-119">Sair da ramificação nos permite ' ressaltar e concluir ' a animação atual antes de chamarmos a próxima animação.</span><span class="sxs-lookup"><span data-stu-id="aa516-119">Exit branching enables us to 'hurry up and finish' the current animation before we call the next animation.</span></span> <span data-ttu-id="aa516-120">Se você não fornecer a ramificação de saída, a transição entre animações pode ser jerky.</span><span class="sxs-lookup"><span data-stu-id="aa516-120">If you don't supply Exit Branching, the transition between animations may be jerky.</span></span>

### <a name="character-properties"></a><span data-ttu-id="aa516-121">Propriedades de caractere</span><span class="sxs-lookup"><span data-stu-id="aa516-121">Character Properties</span></span>

<span data-ttu-id="aa516-122">O Microsoft Agent permite que você defina as propriedades [**Name**](name-property.md), [**Description**](description-property.md) e [**ExtraData**](extradata-property.md) do caractere.</span><span class="sxs-lookup"><span data-stu-id="aa516-122">Microsoft Agent enables you to set the character's [**Name**](name-property.md), [**Description**](description-property.md) and [**ExtraData**](extradata-property.md) properties.</span></span> <span data-ttu-id="aa516-123">Microsoft Office usa o campo **ExtraData** para armazenar uma ou mais frases de introdução e frases de lembrete.</span><span class="sxs-lookup"><span data-stu-id="aa516-123">Microsoft Office uses the **ExtraData** field to hold to one or more Introduction Phrases and Reminder Phrases.</span></span> <span data-ttu-id="aa516-124">Microsoft Office escolhe das outras frases de introdução para colocar no balão de fala na galeria do assistente.</span><span class="sxs-lookup"><span data-stu-id="aa516-124">Microsoft Office picks from the other Introduction Phrases to put in the speech balloon in the Assistant Gallery.</span></span> <span data-ttu-id="aa516-125">Usamos as frases de lembrete quando você recebe um lembrete do Outlook.</span><span class="sxs-lookup"><span data-stu-id="aa516-125">We use the Reminder Phrases when you receive a reminder from Outlook.</span></span>

<span data-ttu-id="aa516-126">O campo [**ExtraData**](extradata-property.md) é formatado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="aa516-126">The [**ExtraData**](extradata-property.md) field is formatted as follows:</span></span>

<span data-ttu-id="aa516-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span><span class="sxs-lookup"><span data-stu-id="aa516-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span></span>

<span data-ttu-id="aa516-128">As frases de introdução são separadas por um par de caracteres de til (~), seguidos por frases de lembrete.</span><span class="sxs-lookup"><span data-stu-id="aa516-128">Intro Phrases are separated by a pair of tilde characters (~), followed by Reminder Phrases.</span></span> <span data-ttu-id="aa516-129">Essas frases de lembrete também são separadas por um par de caracteres de til.</span><span class="sxs-lookup"><span data-stu-id="aa516-129">These Reminder Phrases are also separated by a pair of tilde characters.</span></span> <span data-ttu-id="aa516-130">Os dois conjuntos de frases são separados por dois caracteres de cursor (^^).</span><span class="sxs-lookup"><span data-stu-id="aa516-130">The two sets of phrases are separated by two caret characters (^^).</span></span> <span data-ttu-id="aa516-131">Não há nenhum limite para o número de cada tipo de frase, exceto pelo fato de que deve haver pelo menos um de cada.</span><span class="sxs-lookup"><span data-stu-id="aa516-131">There is no limit to the number of each kind of phrase, except that there must be at least one of each.</span></span>

 

 




