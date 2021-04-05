---
description: A \_ Propriedade PKEY AudioEndpoint \_ ControlPanelPageProvider especifica o CLSID do provedor registrado da extensão de propriedades de dispositivo para o dispositivo de ponto de extremidade de áudio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826406"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a><span data-ttu-id="c2037-103">PKEY \_ AudioEndpoint \_ ControlPanelPageProvider</span><span class="sxs-lookup"><span data-stu-id="c2037-103">PKEY\_AudioEndpoint\_ControlPanelPageProvider</span></span>

<span data-ttu-id="c2037-104">A propriedade **PKEY \_ AudioEndpoint \_ CONTROLPANELPAGEPROVIDER** especifica o CLSID do provedor registrado da extensão de propriedades de dispositivo para o dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="c2037-104">The **PKEY\_AudioEndpoint\_ControlPanelPageProvider** property specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span> <span data-ttu-id="c2037-105">A extensão fornece as propriedades do ponto de extremidade de áudio que são exibidas na página de propriedades do dispositivo do painel de controle multimídia do Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="c2037-105">The extension supplies the audio endpoint properties that are displayed in the device-properties page of the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="c2037-106">Para obter mais informações sobre Mmsys.cpl, consulte a documentação do Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="c2037-106">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="c2037-107">O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="c2037-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="c2037-108">O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID que identifica o provedor da extensão do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c2037-108">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the provider of the control-panel extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2037-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2037-109">Requirements</span></span>



| <span data-ttu-id="c2037-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2037-110">Requirement</span></span> | <span data-ttu-id="c2037-111">Valor</span><span class="sxs-lookup"><span data-stu-id="c2037-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2037-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2037-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c2037-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2037-113">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c2037-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2037-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c2037-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2037-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c2037-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2037-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2037-117"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2037-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2037-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2037-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2037-119">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="c2037-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="c2037-120">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="c2037-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




