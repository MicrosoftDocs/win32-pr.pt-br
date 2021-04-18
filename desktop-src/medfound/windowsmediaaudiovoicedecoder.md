---
description: O decodificador de voz de áudio do Windows Media decodifica os fluxos que foram codificados pelo codificador de voz de áudio do Windows Media.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Decodificador de voz do Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785028"
---
# <a name="windows-media-audio-voice-decoder"></a><span data-ttu-id="ceefd-103">Decodificador de voz do Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="ceefd-103">Windows Media Audio Voice Decoder</span></span>

<span data-ttu-id="ceefd-104">O decodificador de voz de áudio do Windows Media decodifica os fluxos que foram codificados pelo [**codificador de voz de áudio do Windows Media**](windowsmediaaudiovoiceencoder.md).</span><span class="sxs-lookup"><span data-stu-id="ceefd-104">The Windows Media Audio Voice decoder decodes streams that were encoded by the [**Windows Media Audio Voice Encoder**](windowsmediaaudiovoiceencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="ceefd-105">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="ceefd-105">Class Identifier</span></span>

<span data-ttu-id="ceefd-106">O CLSID (identificador de classe) do decodificador de voz de áudio do Windows Media é representado pela constante **CLSID \_ CWMSPDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="ceefd-106">The class identifier (CLSID) for the Windows Media Audio Voice decoder is represented by the constant **CLSID\_CWMSPDecMediaObject**.</span></span> <span data-ttu-id="ceefd-107">Você pode criar uma instância do decodificador de voz chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="ceefd-107">You can create an instance of the voice decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="ceefd-108">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="ceefd-108">Input Formats</span></span>

<span data-ttu-id="ceefd-109">O conteúdo codificado de voz do Windows Media Audio é identificado pela marca de formato 0x00a.</span><span class="sxs-lookup"><span data-stu-id="ceefd-109">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceefd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceefd-110">Requirements</span></span>



| <span data-ttu-id="ceefd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceefd-111">Requirement</span></span> | <span data-ttu-id="ceefd-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ceefd-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ceefd-113">Cliente</span><span class="sxs-lookup"><span data-stu-id="ceefd-113">Client</span></span><br/> | <span data-ttu-id="ceefd-114">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="ceefd-114">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="ceefd-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ceefd-115">Header</span></span><br/> | <dl> <span data-ttu-id="ceefd-116"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceefd-116"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="ceefd-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ceefd-117">DLL</span></span><br/>    | <dl> <span data-ttu-id="ceefd-118"><dt>Wmspdmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ceefd-118"><dt>Wmspdmod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceefd-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceefd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceefd-120">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="ceefd-120">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="ceefd-121">Usando o codec de voz de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="ceefd-121">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="ceefd-122">Codificador de voz do Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="ceefd-122">Windows Media Audio Voice Encoder</span></span>](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




