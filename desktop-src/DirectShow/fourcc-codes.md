---
description: Códigos FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Códigos FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087288"
---
# <a name="fourcc-codes"></a><span data-ttu-id="615a6-103">Códigos FOURCC</span><span class="sxs-lookup"><span data-stu-id="615a6-103">FOURCC Codes</span></span>

<span data-ttu-id="615a6-104">Muitos formatos de mídia digital têm códigos FOURCC atribuídos a eles.</span><span class="sxs-lookup"><span data-stu-id="615a6-104">Many digital media formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="615a6-105">Um código FOURCC é um inteiro sem sinal de 32 bits que é criado pela concatenação de quatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="615a6-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="615a6-106">Por exemplo, o código FOURCC para vídeo YUY2 é ' YUY2 '.</span><span class="sxs-lookup"><span data-stu-id="615a6-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span> <span data-ttu-id="615a6-107">Para formatos de vídeo compactados e formatos de vídeo não RGB (como YUV), o membro de **bicompressão** da estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) deve ser definido como o código FOURCC.</span><span class="sxs-lookup"><span data-stu-id="615a6-107">For compressed video formats and non-RGB video formats (such as YUV), the **biCompression** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure should be set to the FOURCC code.</span></span>

<span data-ttu-id="615a6-108">Há várias macros C/C++ que facilitam a declaração de valores FOURCC no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="615a6-108">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="615a6-109">Por exemplo, a macro **MAKEFOURCC** é declarada em mmsystem. h e a macro **FCC** é declarada em Aviriff. h.</span><span class="sxs-lookup"><span data-stu-id="615a6-109">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="615a6-110">Use-os da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="615a6-110">Use them as follows:</span></span>


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



<span data-ttu-id="615a6-111">Você também pode declarar um código FOURCC diretamente como um literal de cadeia de caracteres simplesmente revertendo a ordem dos caracteres.</span><span class="sxs-lookup"><span data-stu-id="615a6-111">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="615a6-112">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="615a6-112">For example:</span></span>


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



<span data-ttu-id="615a6-113">A reversão do pedido é necessária porque o sistema operacional Microsoft Windows usa uma arquitetura little-endian.</span><span class="sxs-lookup"><span data-stu-id="615a6-113">Reversing the order is necessary because the Microsoft Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="615a6-114">' Y ' = 0x59, ' U ' = 0x55 e ' 2 ' = 0x32, portanto, ' 2YUY ' é 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="615a6-114">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

### <a name="converting-fourcc-codes-to-subtype-guids"></a><span data-ttu-id="615a6-115">Convertendo códigos FOURCC em GUIDs de subtipo</span><span class="sxs-lookup"><span data-stu-id="615a6-115">Converting FOURCC Codes to Subtype GUIDs</span></span>

<span data-ttu-id="615a6-116">Um intervalo de 2 \* GUIDs de 32 é reservado para representar FOURCC.</span><span class="sxs-lookup"><span data-stu-id="615a6-116">A range of 2\*32 GUIDs is reserved for representing FOURCCs.</span></span> <span data-ttu-id="615a6-117">Esses GUIDs são todos os formulários `XXXXXXXX-0000-0010-8000-00AA00389B71` em que `XXXXXXXX` o código FOURCC é.</span><span class="sxs-lookup"><span data-stu-id="615a6-117">These GUIDs are all of the form `XXXXXXXX-0000-0010-8000-00AA00389B71` where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="615a6-118">Portanto, o GUID de subtipo para YUY2 é `32595559-0000-0010-8000-00AA00389B71` .</span><span class="sxs-lookup"><span data-stu-id="615a6-118">Thus, the subtype GUID for YUY2 is `32595559-0000-0010-8000-00AA00389B71`.</span></span>

<span data-ttu-id="615a6-119">Muitas dessas GUIDs já estão definidas no arquivo de cabeçalho UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="615a6-119">Many of these GUIDs are defined already in the header file Uuids.h.</span></span> <span data-ttu-id="615a6-120">Por exemplo, o subtipo YUY2 é definido como MEDIASUBTYPE \_ YUY2.</span><span class="sxs-lookup"><span data-stu-id="615a6-120">For example, the YUY2 subtype is defined as MEDIASUBTYPE\_YUY2.</span></span> <span data-ttu-id="615a6-121">A biblioteca de classes base do DirectShow também fornece uma classe auxiliar, [**FOURCCMap**](fourccmap.md), que pode ser usada para converter códigos FOURCC em valores de GUID.</span><span class="sxs-lookup"><span data-stu-id="615a6-121">The DirectShow base class library also provides a helper class, [**FOURCCMap**](fourccmap.md), which can be used to convert FOURCC codes into GUID values.</span></span> <span data-ttu-id="615a6-122">O construtor **FOURCCMap** usa um código FOURCC como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="615a6-122">The **FOURCCMap** constructor takes a FOURCC code as an input parameter.</span></span> <span data-ttu-id="615a6-123">Em seguida, você pode converter o objeto **FOURCCMap** no GUID correspondente:</span><span class="sxs-lookup"><span data-stu-id="615a6-123">You can then cast the **FOURCCMap** object to the corresponding GUID:</span></span>


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a><span data-ttu-id="615a6-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="615a6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="615a6-125">**Subtipos de áudio**</span><span class="sxs-lookup"><span data-stu-id="615a6-125">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="615a6-126">Subtipos de vídeo</span><span class="sxs-lookup"><span data-stu-id="615a6-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> <dt>

[<span data-ttu-id="615a6-127">Trabalhando com codecs</span><span class="sxs-lookup"><span data-stu-id="615a6-127">Working with Codecs</span></span>](working-with-codecs.md)
</dt> </dl>

 

 



