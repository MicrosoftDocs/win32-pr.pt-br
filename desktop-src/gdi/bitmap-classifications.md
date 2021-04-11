---
description: Classificações de bitmap
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Classificações de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165097"
---
# <a name="bitmap-classifications"></a><span data-ttu-id="f0248-103">Classificações de bitmap</span><span class="sxs-lookup"><span data-stu-id="f0248-103">Bitmap Classifications</span></span>

<span data-ttu-id="f0248-104">Há duas classes de bitmaps:</span><span class="sxs-lookup"><span data-stu-id="f0248-104">There are two classes of bitmaps:</span></span>

-   <span data-ttu-id="f0248-105">DIB ( [bitmaps independentes de dispositivo](device-independent-bitmaps.md) ).</span><span class="sxs-lookup"><span data-stu-id="f0248-105">[Device-independent bitmaps](device-independent-bitmaps.md) (DIB).</span></span> <span data-ttu-id="f0248-106">O formato de arquivo DIB foi projetado para garantir que gráficos de bitmap criados usando um aplicativo possam ser carregados e exibidos em outro aplicativo, mantendo a mesma aparência que o original.</span><span class="sxs-lookup"><span data-stu-id="f0248-106">The DIB file format was designed to ensure that bitmapped graphics created using one application can be loaded and displayed in another application, retaining the same appearance as the original.</span></span>

-   <span data-ttu-id="f0248-107">Os bitmaps [dependentes do dispositivo](device-dependent-bitmaps.md) (BDD), também conhecidos como bitmaps GDI, eram os únicos bitmaps disponíveis nas versões anteriores do Microsoft Windows de 16 bits (antes da versão 3,0).</span><span class="sxs-lookup"><span data-stu-id="f0248-107">[Device-dependent bitmaps](device-dependent-bitmaps.md) (DDB), also known as GDI bitmaps, were the only bitmaps available in early versions of 16-bit Microsoft Windows (prior to version 3.0).</span></span> <span data-ttu-id="f0248-108">No entanto, conforme a tecnologia de exibição melhorou e à medida que a variedade de dispositivos de vídeo disponíveis aumentou, alguns problemas inerentes surgiram, que poderiam ser resolvidos apenas usando DIBs.</span><span class="sxs-lookup"><span data-stu-id="f0248-108">However, as display technology improved and as the variety of available display devices increased, certain inherent problems surfaced which could only be solved using DIBs.</span></span> <span data-ttu-id="f0248-109">Por exemplo, não havia nenhum método de armazenar (ou recuperar) a resolução do tipo de exibição no qual um bitmap foi criado, portanto, um aplicativo de desenho não pôde determinar rapidamente se um bitmap era adequado para o tipo de dispositivo de vídeo no qual o aplicativo estava sendo executado.</span><span class="sxs-lookup"><span data-stu-id="f0248-109">For example, there was no method of storing (or retrieving) the resolution of the display type on which a bitmap was created, so a drawing application could not quickly determine whether a bitmap was suitable for the type of video display device on which the application was running.</span></span>

    <span data-ttu-id="f0248-110">Apesar desses problemas, o DDBs (também conhecido como bitmaps compatíveis) ainda é útil para melhorar o desempenho do GDI e para outras situações.</span><span class="sxs-lookup"><span data-stu-id="f0248-110">Despite these problems, DDBs (also known as compatible bitmaps) are still useful for better GDI performance and for other situations.</span></span>

 

 



