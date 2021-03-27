---
description: O atributo Pattern especifica o padrão de uma caneta geométrica.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Padrão de caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502404"
---
# <a name="pen-pattern"></a><span data-ttu-id="1434b-103">Padrão de caneta</span><span class="sxs-lookup"><span data-stu-id="1434b-103">Pen Pattern</span></span>

<span data-ttu-id="1434b-104">O atributo Pattern especifica o padrão de uma caneta geométrica.</span><span class="sxs-lookup"><span data-stu-id="1434b-104">The pattern attribute specifies the pattern of a geometric pen.</span></span>

<span data-ttu-id="1434b-105">A ilustração a seguir mostra linhas desenhadas com canetas geométricas diferentes.</span><span class="sxs-lookup"><span data-stu-id="1434b-105">The following illustration shows lines drawn with different geometric pens.</span></span> <span data-ttu-id="1434b-106">Cada caneta foi criada usando um atributo de padrão diferente.</span><span class="sxs-lookup"><span data-stu-id="1434b-106">Each pen was created using a different pattern attribute.</span></span>

![ilustração mostrando quatro linhas, cada uma preenchida com uma caneta diferente](images/cspen-02.png)

<span data-ttu-id="1434b-108">A primeira linha da ilustração anterior é desenhada usando um dos seis padrões de hachura disponíveis; para obter mais informações sobre padrões de hachura, consulte [hachura](pen-hatch.md).</span><span class="sxs-lookup"><span data-stu-id="1434b-108">The first line in the previous illustration is drawn using one of the six available hatch patterns; for more information about hatch patterns, see [Pen Hatch](pen-hatch.md).</span></span> <span data-ttu-id="1434b-109">A próxima linha é desenhada usando o padrão vazio, idêntico ao padrão NULL.</span><span class="sxs-lookup"><span data-stu-id="1434b-109">The next line is drawn using the hollow pattern, identical to the null pattern.</span></span> <span data-ttu-id="1434b-110">A terceira linha é desenhada usando um padrão personalizado criado a partir de um bitmap de 8 por 8 pixels.</span><span class="sxs-lookup"><span data-stu-id="1434b-110">The third line is drawn using a custom pattern created from an 8-by-8-pixel bitmap.</span></span> <span data-ttu-id="1434b-111">(Para obter mais informações sobre bitmaps e sua criação, consulte [bitmaps](bitmaps.md).) A última linha é desenhada usando um padrão sólido.</span><span class="sxs-lookup"><span data-stu-id="1434b-111">(For more information about bitmaps and their creation, see [Bitmaps](bitmaps.md).) The last line is drawn using a solid pattern.</span></span> <span data-ttu-id="1434b-112">Criar um pincel e passar seu identificador para a função [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) cria um padrão.</span><span class="sxs-lookup"><span data-stu-id="1434b-112">Creating a brush and passing its handle to the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function creates a pattern.</span></span>

 

 



