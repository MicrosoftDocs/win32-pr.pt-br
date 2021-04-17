---
description: O método getvideoclipize recupera as dimensões de vídeo nativas.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Método getvídeos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105782245"
---
# <a name="getvideosize-method"></a><span data-ttu-id="d38c0-103">Método getvídeos</span><span class="sxs-lookup"><span data-stu-id="d38c0-103">GetVideoSize Method</span></span>

> [!Note]  
> <span data-ttu-id="d38c0-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d38c0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d38c0-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d38c0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d38c0-106">O `GetVideoSize` método recupera as dimensões de vídeo nativas.</span><span class="sxs-lookup"><span data-stu-id="d38c0-106">The `GetVideoSize` method retrieves the native video dimensions.</span></span>

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a><span data-ttu-id="d38c0-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d38c0-107">Return Value</span></span>

<span data-ttu-id="d38c0-108">Retorna um objeto [DVDRect](dvdrect-object.md) contendo quatro propriedades de leitura/gravação: (superior esquerda) x; (superior esquerda) y, largura e altura.</span><span class="sxs-lookup"><span data-stu-id="d38c0-108">Returns a [DVDRect](dvdrect-object.md) object containing four read/write properties: (top left) x; (top left) y, Width, and Height.</span></span> <span data-ttu-id="d38c0-109">As propriedades **x** e **y** são definidas como zero e as outras duas propriedades refletem a largura e a altura do retângulo de vídeo como sendo criados no disco.</span><span class="sxs-lookup"><span data-stu-id="d38c0-109">The **x** and **y** properties are set to zero and the other two properties reflect the width and height of the video rectangle as authored on the disc.</span></span>

 

 



