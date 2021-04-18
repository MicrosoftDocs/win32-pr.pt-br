---
description: Este tópico descreve como buscar durante a reprodução usando o MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Como buscar durante a reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789477"
---
# <a name="how-to-seek-during-playback"></a><span data-ttu-id="6bda9-103">Como buscar durante a reprodução</span><span class="sxs-lookup"><span data-stu-id="6bda9-103">How to Seek During Playback</span></span>

<span data-ttu-id="6bda9-104">\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6bda9-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6bda9-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6bda9-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6bda9-106">\]</span><span class="sxs-lookup"><span data-stu-id="6bda9-106">\]</span></span>

<span data-ttu-id="6bda9-107">Este tópico descreve como buscar durante a reprodução usando o MFPlay.</span><span class="sxs-lookup"><span data-stu-id="6bda9-107">This topic describes how to seek during playback using MFPlay.</span></span>

<span data-ttu-id="6bda9-108">**Para buscar durante a reprodução**</span><span class="sxs-lookup"><span data-stu-id="6bda9-108">**To Seek During Playback**</span></span>

1.  <span data-ttu-id="6bda9-109">Inicialize um **PROPVARIANT** para manter o tempo de busca em unidades de 100 nanossegundos, como um tipo **\_ inteiro** (**VT \_ i8**).</span><span class="sxs-lookup"><span data-stu-id="6bda9-109">Initialize a **PROPVARIANT** to hold the seek time in 100-nanosecond units, as a **LARGE\_INTEGER** (**VT\_I8**) type.</span></span>
2.  <span data-ttu-id="6bda9-110">Chame [**IMFPMediaPlayer:: SETPOSITION**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span><span class="sxs-lookup"><span data-stu-id="6bda9-110">Call [**IMFPMediaPlayer::SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span></span> <span data-ttu-id="6bda9-111">Especifique **o \_ PositionType do MFP de \_ 100 NS** para o primeiro parâmetro e passe o **PROPVARIANT** para o segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6bda9-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter, and pass in the **PROPVARIANT** for the second parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bda9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bda9-112">Requirements</span></span>

<span data-ttu-id="6bda9-113">O MFPlay requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6bda9-113">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bda9-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6bda9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bda9-115">Usando o MFPlay para reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="6bda9-115">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



