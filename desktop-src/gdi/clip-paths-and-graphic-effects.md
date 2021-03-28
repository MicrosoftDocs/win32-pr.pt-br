---
description: Um aplicativo pode usar recorte e caminhos para criar efeitos gráficos especiais. A ilustração a seguir mostra uma cadeia de texto desenhada com uma fonte Arial grande.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Caminhos de clipes e efeitos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502435"
---
# <a name="clip-paths-and-graphic-effects"></a><span data-ttu-id="09fe0-104">Caminhos de clipes e efeitos gráficos</span><span class="sxs-lookup"><span data-stu-id="09fe0-104">Clip Paths and Graphic Effects</span></span>

<span data-ttu-id="09fe0-105">Um aplicativo pode usar recorte e caminhos para criar efeitos gráficos especiais.</span><span class="sxs-lookup"><span data-stu-id="09fe0-105">An application can use clipping and paths to create special graphic effects.</span></span> <span data-ttu-id="09fe0-106">A ilustração a seguir mostra uma cadeia de texto desenhada com uma fonte Arial grande.</span><span class="sxs-lookup"><span data-stu-id="09fe0-106">The following illustration shows a string of text drawn with a large Arial font.</span></span>

![ilustração mostrando texto preto em um plano de fundo branco](images/cspth-02.png)

<span data-ttu-id="09fe0-108">A ilustração a seguir mostra o resultado da seleção do texto como um caminho de clipe e o desenho de linhas radiais para um círculo cujo centro está localizado acima e à esquerda da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="09fe0-108">The next illustration shows the result of selecting the text as a clip path and drawing radial lines for a circle whose center is located above and left of the string.</span></span>

![ilustração mostrando o mesmo texto, mas preenchido com linhas em vez de preto sólido](images/cspth-03.png)

> [!Note]  
> <span data-ttu-id="09fe0-110">Antes da interface de dispositivo de gráficos (GDI) adicionar texto criado com uma fonte de bitmap a um caminho, ele converte a fonte em um contorno ou em uma fonte de vetor.</span><span class="sxs-lookup"><span data-stu-id="09fe0-110">Before graphics device interface (GDI) adds text created with a bitmapped font to a path, it converts the font to an outline or vector font.</span></span>

 

<span data-ttu-id="09fe0-111">Um aplicativo cria um caminho de clipe gerando um colchete de caminho e, em seguida, chamando a função [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) .</span><span class="sxs-lookup"><span data-stu-id="09fe0-111">An application creates a clip path by generating a path bracket and then calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function.</span></span> <span data-ttu-id="09fe0-112">Depois que um caminho de clipe é selecionado em um DC, a saída aparece apenas dentro das bordas do caminho.</span><span class="sxs-lookup"><span data-stu-id="09fe0-112">After a clip path is selected into a DC, output only appears within the borders of the path.</span></span>

<span data-ttu-id="09fe0-113">Além de criar efeitos gráficos especiais, os caminhos de clipes também são úteis em aplicativos que salvam imagens como metaarquivos aprimorados.</span><span class="sxs-lookup"><span data-stu-id="09fe0-113">In addition to creating special graphics effects, clip paths are also useful in applications that save images as enhanced metafiles.</span></span> <span data-ttu-id="09fe0-114">Usando um caminho de clipe, um aplicativo é capaz de garantir a independência do dispositivo, pois as unidades usadas para especificar um caminho são unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="09fe0-114">By using a clip path, an application is able to ensure device independence because the units used to specify a path are logical units.</span></span>

 

 



