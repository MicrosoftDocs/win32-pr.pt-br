---
description: Tempo limite de rotação da unidade de DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Tempo limite de rotação da unidade de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825925"
---
# <a name="dvd-drive-spin-down-timeout"></a><span data-ttu-id="d5727-103">Tempo limite de rotação da unidade de DVD</span><span class="sxs-lookup"><span data-stu-id="d5727-103">DVD Drive Spin Down Timeout</span></span>

<span data-ttu-id="d5727-104">Em computadores laptop, para conservar a vida útil da bateria, pode ser desejável reduzir o período de tempo que uma unidade de DVD continuará a girar depois que o usuário tiver pausado a reprodução.</span><span class="sxs-lookup"><span data-stu-id="d5727-104">On laptop computers, to conserve battery life it may be desirable to reduce the length of time that a DVD drive will continue to spin after the user has paused playback.</span></span> <span data-ttu-id="d5727-105">Por padrão, o navegador de DVD mantém o disco girando por dois minutos.</span><span class="sxs-lookup"><span data-stu-id="d5727-105">By default, the DVD Navigator keeps the disc spinning for two minutes.</span></span> <span data-ttu-id="d5727-106">Esse valor pode ser modificado no registro do Windows sob esta chave:</span><span class="sxs-lookup"><span data-stu-id="d5727-106">This value can be modified in the Windows Registry under this key:</span></span>


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



<span data-ttu-id="d5727-107">onde</span><span class="sxs-lookup"><span data-stu-id="d5727-107">where</span></span>


```
Sec
```



<span data-ttu-id="d5727-108">é o tempo de desativação de rotação em segundos.</span><span class="sxs-lookup"><span data-stu-id="d5727-108">is the spin down time in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5727-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5727-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5727-110">Apêndices</span><span class="sxs-lookup"><span data-stu-id="d5727-110">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



