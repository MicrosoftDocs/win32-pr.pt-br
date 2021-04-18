---
description: Definindo a taxa de reprodução
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Definindo a taxa de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105767668"
---
# <a name="setting-the-playback-rate"></a><span data-ttu-id="fd30e-103">Definindo a taxa de reprodução</span><span class="sxs-lookup"><span data-stu-id="fd30e-103">Setting the Playback Rate</span></span>

<span data-ttu-id="fd30e-104">Para alterar a taxa de reprodução, chame o método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="fd30e-104">To change the playback rate, call the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span> <span data-ttu-id="fd30e-105">Especifique a nova taxa como uma fração da taxa original.</span><span class="sxs-lookup"><span data-stu-id="fd30e-105">Specify the new rate as a fraction of the original rate.</span></span> <span data-ttu-id="fd30e-106">Por exemplo, para reproduzir em velocidade de duas vezes-normal, use o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fd30e-106">For example, to play at twice-normal speed, use the following:</span></span>


```C++
pSeek->SetRate(2.0)
```



<span data-ttu-id="fd30e-107">As taxas maiores que um são mais rápidas do que o normal.</span><span class="sxs-lookup"><span data-stu-id="fd30e-107">Rates greater than one are faster than normal.</span></span> <span data-ttu-id="fd30e-108">As taxas entre zero e uma são mais lentas do que o normal.</span><span class="sxs-lookup"><span data-stu-id="fd30e-108">Rates between zero and one are slower than normal.</span></span> <span data-ttu-id="fd30e-109">As taxas negativas são definidas como reprodução regressiva, mas na prática a maioria dos filtros não oferece suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="fd30e-109">Negative rates are defined as backward playback, but in practice most filters do not support it.</span></span> <span data-ttu-id="fd30e-110">Atualmente, nenhum dos filtros do DirectShow padrão oferece suporte à reprodução inversa.</span><span class="sxs-lookup"><span data-stu-id="fd30e-110">Currently none of the standard DirectShow filters support reverse playback.</span></span>

<span data-ttu-id="fd30e-111">Independentemente da taxa de reprodução, a posição atual e a posição de parada são sempre expressas em relação à fonte original.</span><span class="sxs-lookup"><span data-stu-id="fd30e-111">Regardless of the playback rate, the current position and the stop position are always expressed relative to the original source.</span></span> <span data-ttu-id="fd30e-112">Por exemplo, se um arquivo de origem tiver 20 segundos de duração na taxa de reprodução normal, definir a posição atual como 10 segundos irá procurar o meio do arquivo.</span><span class="sxs-lookup"><span data-stu-id="fd30e-112">For example, if a source file is 20 seconds long at normal playback rate, setting the current position to 10 seconds will seek to the middle of the file.</span></span> <span data-ttu-id="fd30e-113">Se a taxa de reprodução for 2,0, a posição de parada será de 20 segundos e você procurar a posição de 10 segundos, o arquivo será executado por 5 minutos de tempo real: 10 segundos de importância, com duas vezes a velocidade de reprodução normal.</span><span class="sxs-lookup"><span data-stu-id="fd30e-113">If the playback rate is 2.0, the stop position is 20 seconds, and you seek to the 10-second position, the file will play for 5 seconds of real time: 10 seconds' worth, at twice the normal playback speed.</span></span> <span data-ttu-id="fd30e-114">Em uma taxa de reprodução de 2,0, a posição atual aumenta em duas vezes a taxa do relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="fd30e-114">At a playback rate of 2.0, the current position increases at twice the rate of the reference clock.</span></span>

 

 



