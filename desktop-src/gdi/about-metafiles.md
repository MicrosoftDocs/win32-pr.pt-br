---
description: Internamente, um metarquivo é uma matriz de estruturas de comprimento variável chamada registros de metarquivo.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Sobre os metaarquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647673"
---
# <a name="about-metafiles"></a><span data-ttu-id="916a8-103">Sobre os metaarquivos</span><span class="sxs-lookup"><span data-stu-id="916a8-103">About Metafiles</span></span>

<span data-ttu-id="916a8-104">Internamente, um metarquivo é uma matriz de estruturas de comprimento variável chamada *registros de metarquivo*.</span><span class="sxs-lookup"><span data-stu-id="916a8-104">Internally, a metafile is an array of variable-length structures called *metafile records*.</span></span> <span data-ttu-id="916a8-105">Os primeiros registros no metarquivo especificam informações gerais, como a resolução do dispositivo no qual a imagem foi criada, as dimensões da imagem e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="916a8-105">The first records in the metafile specify general information such as the resolution of the device on which the picture was created, the dimensions of the picture, and so on.</span></span> <span data-ttu-id="916a8-106">Os registros restantes, que constituem a massa de qualquer metarquivo, correspondem às funções da interface de dispositivo de gráficos (GDI) necessárias para desenhar a imagem.</span><span class="sxs-lookup"><span data-stu-id="916a8-106">The remaining records, which constitute the bulk of any metafile, correspond to the graphics device interface (GDI) functions required to draw the picture.</span></span> <span data-ttu-id="916a8-107">Esses registros são armazenados no metarquivo após a criação de um contexto de dispositivo de metarquivo especial.</span><span class="sxs-lookup"><span data-stu-id="916a8-107">These records are stored in the metafile after a special metafile device context is created.</span></span> <span data-ttu-id="916a8-108">Esse contexto de dispositivo de metarquivo é usado em seguida para todas as operações de desenho necessárias para criar a imagem.</span><span class="sxs-lookup"><span data-stu-id="916a8-108">This metafile device context is then used for all drawing operations required to create the picture.</span></span> <span data-ttu-id="916a8-109">Quando o sistema processa uma função GDI associada a um DC de metarquivo, ele converte a função nos dados apropriados e armazena esses dados em um registro anexado ao metarquivo.</span><span class="sxs-lookup"><span data-stu-id="916a8-109">When the system processes a GDI function associated with a metafile DC, it converts the function into the appropriate data and stores this data in a record appended to the metafile.</span></span>

<span data-ttu-id="916a8-110">Depois que uma imagem for concluída e o último registro for armazenado no metarquivo, você poderá passar o metarquivo para outro aplicativo:</span><span class="sxs-lookup"><span data-stu-id="916a8-110">After a picture is complete and the last record is stored in the metafile, you can pass the metafile to another application by:</span></span>

-   <span data-ttu-id="916a8-111">Usando a área de transferência</span><span class="sxs-lookup"><span data-stu-id="916a8-111">Using the clipboard</span></span>
-   <span data-ttu-id="916a8-112">Inserindo-o em outro arquivo</span><span class="sxs-lookup"><span data-stu-id="916a8-112">Embedding it within another file</span></span>
-   <span data-ttu-id="916a8-113">Armazenando em disco</span><span class="sxs-lookup"><span data-stu-id="916a8-113">Storing it on disk</span></span>
-   <span data-ttu-id="916a8-114">Jogando repetidamente</span><span class="sxs-lookup"><span data-stu-id="916a8-114">Playing it repeatedly</span></span>

<span data-ttu-id="916a8-115">Um metarquivo é *reproduzido* quando seus registros são convertidos em comandos de dispositivo e processados pelo dispositivo apropriado.</span><span class="sxs-lookup"><span data-stu-id="916a8-115">A metafile is *played* when its records are converted to device commands and processed by the appropriate device.</span></span>

<span data-ttu-id="916a8-116">Há dois tipos de metaarquivos:</span><span class="sxs-lookup"><span data-stu-id="916a8-116">There are two types of metafiles:</span></span>

-   [<span data-ttu-id="916a8-117">Metarquivos de formato avançado</span><span class="sxs-lookup"><span data-stu-id="916a8-117">Enhanced-format metafiles</span></span>](enhanced-format-metafiles.md)
-   [<span data-ttu-id="916a8-118">Metaarquivos de formato do Windows</span><span class="sxs-lookup"><span data-stu-id="916a8-118">Windows-format metafiles</span></span>](windows-format-metafiles.md)

 

 



