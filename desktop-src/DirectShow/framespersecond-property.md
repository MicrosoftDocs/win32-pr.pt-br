---
description: A propriedade FramesPerSecond recupera a taxa de quadros de vídeo para o título do DVD atual.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Propriedade FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105782246"
---
# <a name="framespersecond-property"></a><span data-ttu-id="3f9db-103">Propriedade FramesPerSecond</span><span class="sxs-lookup"><span data-stu-id="3f9db-103">FramesPerSecond Property</span></span>

> [!Note]  
> <span data-ttu-id="3f9db-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3f9db-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3f9db-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="3f9db-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3f9db-106">A `FramesPerSecond` propriedade recupera a taxa de quadros de vídeo para o título do DVD atual.</span><span class="sxs-lookup"><span data-stu-id="3f9db-106">The `FramesPerSecond` property retrieves the video frame rate for the current DVD title.</span></span>

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a><span data-ttu-id="3f9db-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3f9db-107">Return Value</span></span>

<span data-ttu-id="3f9db-108">Retorna um valor inteiro que representa a taxa de quadros de vídeo; 25 ou 30 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="3f9db-108">Returns an integer value representing the video frame rate; either 25 or 30 frames per second.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f9db-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f9db-109">Remarks</span></span>

<span data-ttu-id="3f9db-110">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="3f9db-110">This property is read-only with no default value.</span></span> <span data-ttu-id="3f9db-111">Os sinais de vídeo NTSC são exibidos em 30 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="3f9db-111">NTSC video signals are displayed at 30 frames per second.</span></span> <span data-ttu-id="3f9db-112">PAL é exibido em 25 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="3f9db-112">PAL is displayed at 25 frames per second.</span></span> <span data-ttu-id="3f9db-113">Um disco é codificado para reprodução em NTSC ou PAL, mas não pode ser executado em ambos.</span><span class="sxs-lookup"><span data-stu-id="3f9db-113">A disc is encoded to play on either NTSC or PAL, but cannot play on both.</span></span>

 

 



