---
description: A \_ Propriedade PKEY AudioEndpoint \_ JackSubType contém um GUID de categoria de saída para um dispositivo de ponto de extremidade de áudio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089515"
---
# <a name="pkey_audioendpoint_jacksubtype"></a><span data-ttu-id="72166-103">PKEY \_ AudioEndpoint \_ JackSubType</span><span class="sxs-lookup"><span data-stu-id="72166-103">PKEY\_AudioEndpoint\_JackSubType</span></span>

<span data-ttu-id="72166-104">A propriedade **PKEY \_ AudioEndpoint \_ JACKSUBTYPE** contém um GUID de categoria de saída para um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="72166-104">The **PKEY\_AudioEndpoint\_JackSubType** property contains an output category GUID for an audio endpoint device.</span></span> <span data-ttu-id="72166-105">O arquivo de cabeçalho Ksmedia. h define os GUIDs; cada GUID especifica o tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="72166-105">The header file Ksmedia.h defines the GUIDs; each GUID specifies the type of connection.</span></span> <span data-ttu-id="72166-106">Esses GUIDs também têm categorias de PIN associadas.</span><span class="sxs-lookup"><span data-stu-id="72166-106">These GUIDs also have associated pin categories.</span></span> <span data-ttu-id="72166-107">Por exemplo, o arquivo de cabeçalho Ksmedia. h define **a \_ \_ interface do GUID KSNODETYPE DisplayPort** para uma porta de exibição que se conecta com o PIN KS definido pelo GUID **PINNAME \_ DisplayPort \_ out**.</span><span class="sxs-lookup"><span data-stu-id="72166-107">For example, header file Ksmedia.h defines the GUID **KSNODETYPE\_DISPLAYPORT\_INTERFACE** for a display port that connects with the KS pin defined by the GUID **PINNAME\_DISPLAYPORT\_OUT**.</span></span>

<span data-ttu-id="72166-108">Para obter mais informações, consulte a descrição das propriedades de categoria do PIN na documentação do Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="72166-108">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="72166-109">O membro **VT** da estrutura **PROPVARIANT** é definido como **VT \_ LPWSTR**.</span><span class="sxs-lookup"><span data-stu-id="72166-109">The **vt** member of the **PROPVARIANT** structure is set to **VT\_LPWSTR**.</span></span>

<span data-ttu-id="72166-110">O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID de categoria.</span><span class="sxs-lookup"><span data-stu-id="72166-110">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="72166-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72166-111">Requirements</span></span>



| <span data-ttu-id="72166-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="72166-112">Requirement</span></span> | <span data-ttu-id="72166-113">Valor</span><span class="sxs-lookup"><span data-stu-id="72166-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72166-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72166-114">Minimum supported client</span></span><br/> | <span data-ttu-id="72166-115">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="72166-115">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="72166-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72166-116">Minimum supported server</span></span><br/> | <span data-ttu-id="72166-117">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="72166-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72166-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72166-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="72166-119"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="72166-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72166-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="72166-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72166-121">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="72166-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="72166-122">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="72166-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




