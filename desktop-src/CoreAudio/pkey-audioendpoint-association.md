---
description: A \_ propriedade de associação PKEY AudioEndpoint \_ associa uma categoria de PIN de streaming de kernel (KS) a um dispositivo de ponto de extremidade de áudio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756018"
---
# <a name="pkey_audioendpoint_association"></a><span data-ttu-id="345c2-103">PKEY \_ AudioEndpoint \_ Association</span><span class="sxs-lookup"><span data-stu-id="345c2-103">PKEY\_AudioEndpoint\_Association</span></span>

<span data-ttu-id="345c2-104">A propriedade de **\_ \_ Associação PKEY AudioEndpoint** associa uma categoria de PIN de streaming de kernel (KS) a um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="345c2-104">The **PKEY\_AudioEndpoint\_Association** property associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span> <span data-ttu-id="345c2-105">O arquivo. inf que instala um adaptador de áudio atribui uma categoria de PIN a cada PIN KS no adaptador.</span><span class="sxs-lookup"><span data-stu-id="345c2-105">The .inf file that installs an audio adapter assigns a pin category to each KS pin in the adapter.</span></span> <span data-ttu-id="345c2-106">Um PIN KS em um dispositivo de adaptador representa o ponto em que um fluxo de áudio entra ou sai do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="345c2-106">A KS pin on an adapter device represents the point at which an audio stream enters or leaves the device.</span></span> <span data-ttu-id="345c2-107">Uma categoria de PIN é um GUID que especifica o tipo de função executada por um PIN KS.</span><span class="sxs-lookup"><span data-stu-id="345c2-107">A pin category is a GUID that specifies the type of function performed by a KS pin.</span></span> <span data-ttu-id="345c2-108">Por exemplo, o arquivo de cabeçalho Ksmedia. h define o PIN da categoria de fixação KSNODETYPE \_ microfone para indicar um PIN KS que se conecta a um microfone e \_ fone de ouvido para indicar um PIN KS que se conecta aos fones de ouvido.</span><span class="sxs-lookup"><span data-stu-id="345c2-108">For example, header file Ksmedia.h defines pin-category GUID KSNODETYPE\_MICROPHONE to indicate a KS pin that connects to a microphone, and KSNODETYPE\_HEADPHONES to indicate a KS pin that connects to headphones.</span></span> <span data-ttu-id="345c2-109">Para obter mais informações, consulte a descrição das propriedades de categoria do PIN na documentação do Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="345c2-109">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="345c2-110">O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="345c2-110">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="345c2-111">O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID de categoria de PIN KS.</span><span class="sxs-lookup"><span data-stu-id="345c2-111">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a KS pin category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="345c2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="345c2-112">Requirements</span></span>



| <span data-ttu-id="345c2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="345c2-113">Requirement</span></span> | <span data-ttu-id="345c2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="345c2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="345c2-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="345c2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="345c2-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="345c2-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="345c2-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="345c2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="345c2-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="345c2-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="345c2-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="345c2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="345c2-120"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="345c2-120"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="345c2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="345c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345c2-122">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="345c2-122">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="345c2-123">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="345c2-123">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




