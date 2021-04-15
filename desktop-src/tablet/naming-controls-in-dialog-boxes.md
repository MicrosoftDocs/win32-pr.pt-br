---
description: Ao usar as caixas de diálogo do Microsoft Windows, você deve rotular todos os controles para facilitar a funcionalidade de fala. A caixa de diálogo Executar seguinte mostra um rótulo de controle de texto estático para uma caixa de listagem suspensa. O texto estático termina com dois-pontos.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Controles de nomenclatura em caixas de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570207"
---
# <a name="naming-controls-in-dialog-boxes"></a><span data-ttu-id="4c7dd-105">Controles de nomenclatura em caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="4c7dd-105">Naming Controls in Dialog Boxes</span></span>

<span data-ttu-id="4c7dd-106">Ao usar as caixas de diálogo do Microsoft Windows, você deve rotular todos os controles para facilitar a funcionalidade de fala.</span><span class="sxs-lookup"><span data-stu-id="4c7dd-106">When using Microsoft Windows dialog boxes, you must label all controls to facilitate speech functionality.</span></span> <span data-ttu-id="4c7dd-107">A caixa de diálogo **executar** seguinte mostra um rótulo de controle de texto estático para uma caixa de listagem suspensa.</span><span class="sxs-lookup"><span data-stu-id="4c7dd-107">The following **Run** dialog box shows a static text control label for a drop-down list box.</span></span> <span data-ttu-id="4c7dd-108">O texto estático termina com dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="4c7dd-108">Static text ends with a colon.</span></span>

![captura de tela mostrando a caixa de diálogo Executar](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

<span data-ttu-id="4c7dd-110">Há dois tipos de controle:</span><span class="sxs-lookup"><span data-stu-id="4c7dd-110">There are two types of controls:</span></span>

-   <span data-ttu-id="4c7dd-111">Controles que têm suas legendas como uma propriedade desse controle, como botões de comando e caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="4c7dd-111">Controls that have their captions as a property of that control, such as command buttons and check boxes.</span></span> <span data-ttu-id="4c7dd-112">Os recursos de acessibilidade não têm problemas para identificar esses controles, desde que a legenda esteja definida corretamente.</span><span class="sxs-lookup"><span data-stu-id="4c7dd-112">Accessibility aids have no trouble identifying these controls as long as the caption is properly defined.</span></span>
-   <span data-ttu-id="4c7dd-113">Controles que não têm suas próprias legendas, como controles de edição, caixas de listagem e exibições de lista, devem ser rotulados usando controles de texto estáticos separados.</span><span class="sxs-lookup"><span data-stu-id="4c7dd-113">Controls that do not have their own captions, such as edit controls, list boxes and list views, must be labeled by using separate static text controls.</span></span> <span data-ttu-id="4c7dd-114">Para obter mais informações sobre controles que não têm suas próprias legendas, consulte [controles sem propriedades de legenda](controls-without-caption-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4c7dd-114">For more information about controls that do not have their own captions, see [Controls Without Caption Properties](controls-without-caption-properties.md).</span></span>

<span data-ttu-id="4c7dd-115">Várias técnicas podem ser usadas para superar situações nas quais os controles não têm suas próprias legendas, mas são apenas eficazes para janelas que são exibidas pelo SDM (Gerenciador de caixas de diálogo padrão).</span><span class="sxs-lookup"><span data-stu-id="4c7dd-115">Several techniques can be used to overcome situations in which controls do not have their own captions, but they are only effective for windows that are displayed by the Standard Dialog Manager (SDM).</span></span> <span data-ttu-id="4c7dd-116">Todas as outras janelas precisam expor os nomes e a relação entre os controles com suporte explícito ao Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="4c7dd-116">All other windows need to expose the names and relationship between controls by explicitly supporting Microsoft Active Accessibility.</span></span> <span data-ttu-id="4c7dd-117">Para obter mais informações sobre Acessibilidade Ativa, consulte a seção [acessibilidade](/windows/desktop/accessibility) da biblioteca MSDN.</span><span class="sxs-lookup"><span data-stu-id="4c7dd-117">For more information about Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section of the MSDN Library.</span></span>

 

 
