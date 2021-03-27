---
description: O atributo Style especifica o padrão de linha que aparece quando uma caneta superficial ou geométrica específica é usada. Há oito estilos de caneta predefinidos. A ilustração a seguir mostra os sete desses estilos que são definidos pelo sistema.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Estilo da caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921285"
---
# <a name="pen-style"></a><span data-ttu-id="e7c1a-105">Estilo da caneta</span><span class="sxs-lookup"><span data-stu-id="e7c1a-105">Pen Style</span></span>

<span data-ttu-id="e7c1a-106">O atributo Style especifica o padrão de linha que aparece quando uma caneta superficial ou geométrica específica é usada.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-106">The style attribute specifies the line pattern that appears when a particular cosmetic or geometric pen is used.</span></span> <span data-ttu-id="e7c1a-107">Há oito estilos de caneta predefinidos.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-107">There are eight predefined pen styles.</span></span> <span data-ttu-id="e7c1a-108">A ilustração a seguir mostra os sete desses estilos que são definidos pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-108">The following illustration shows the seven of these styles that are defined by the system.</span></span>

![ilustração mostrando sete linhas, cada uma desenhada usando um estilo predefinido diferente](images/cspen-01.png)

<span data-ttu-id="e7c1a-110">O estilo de quadro interno é idêntico ao estilo sólido para canetas superficiais.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-110">The inside-frame style is identical to the solid style for cosmetic pens.</span></span> <span data-ttu-id="e7c1a-111">No entanto, ele funciona de forma diferente quando usado com uma caneta geométrica.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-111">However, it operates differently when used with a geometric pen.</span></span> <span data-ttu-id="e7c1a-112">Se a caneta geométrica for mais ampla do que um único pixel e uma função de desenho usar a caneta para desenhar uma borda em torno de um objeto preenchido, o sistema desenhará a borda dentro do quadro do objeto.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-112">If the geometric pen is wider than a single pixel and a drawing function uses the pen to draw a border around a filled object, the system draws the border inside the object's frame.</span></span> <span data-ttu-id="e7c1a-113">Usando o estilo de quadro interno, um aplicativo pode garantir que um objeto apareça inteiramente dentro das dimensões especificadas, independentemente da largura da caneta geométrica.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-113">By using the inside-frame style, an application can ensure that an object appears entirely within the specified dimensions, regardless of the geometric pen width.</span></span>

<span data-ttu-id="e7c1a-114">Além dos sete estilos definidos pelo sistema, há um oitavo estilo definido pelo usuário (ou aplicativo).</span><span class="sxs-lookup"><span data-stu-id="e7c1a-114">In addition to the seven styles defined by the system, there is an eighth style that is user (or application) defined.</span></span> <span data-ttu-id="e7c1a-115">Um estilo definido pelo usuário gera linhas com uma série personalizada de traços e pontos.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-115">A user-defined style generates lines with a customized series of dashes and dots.</span></span>

<span data-ttu-id="e7c1a-116">Use a função [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) para criar uma caneta que tenha os estilos definidos pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-116">Use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function to create a pen that has the system-defined styles.</span></span> <span data-ttu-id="e7c1a-117">Use a função **ExtCreatePen** para criar uma caneta que tenha um estilo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e7c1a-117">Use the **ExtCreatePen** function to create a pen that has a user-defined style.</span></span>

 

 



