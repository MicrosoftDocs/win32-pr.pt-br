---
description: A propriedade volume define ou recupera o volume do alto-falante para a saída do fluxo de áudio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Propriedade Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502240"
---
# <a name="volume-property"></a><span data-ttu-id="56cc3-103">Propriedade Volume</span><span class="sxs-lookup"><span data-stu-id="56cc3-103">Volume Property</span></span>

> [!Note]  
> <span data-ttu-id="56cc3-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56cc3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="56cc3-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="56cc3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="56cc3-106">A `Volume` propriedade define ou recupera o volume do alto-falante para a saída do fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="56cc3-106">The `Volume` property sets or retrieves the speaker volume for the audio stream output.</span></span>

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a><span data-ttu-id="56cc3-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="56cc3-107">Return Value</span></span>

<span data-ttu-id="56cc3-108">Retorna o nível de volume como atenuação em decibéis como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="56cc3-108">Returns the volume level as attenuation in decibels as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="56cc3-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="56cc3-109">Remarks</span></span>

<span data-ttu-id="56cc3-110">Essa propriedade é de leitura/gravação com um valor padrão de 0.</span><span class="sxs-lookup"><span data-stu-id="56cc3-110">This property is read/write with a default value of 0.</span></span> <span data-ttu-id="56cc3-111">O volume completo é 0 e 10.000 é silêncio; a escala é logarítmica.</span><span class="sxs-lookup"><span data-stu-id="56cc3-111">Full volume is 0, and 10,000 is silence; the scale is logarithmic.</span></span> <span data-ttu-id="56cc3-112">Multiplique o nível de decibéi desejado por 100 (por exemplo, 10.000 = 100 dB).</span><span class="sxs-lookup"><span data-stu-id="56cc3-112">Multiply the desired decibel level by 100 (for example 10,000 = 100 dB).</span></span>

 

 



