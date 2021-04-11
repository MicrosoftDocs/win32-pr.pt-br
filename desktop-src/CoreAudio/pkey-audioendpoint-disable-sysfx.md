---
description: A \_ Propriedade PKEY AudioEndpoint \_ Disable \_ SysFx especifica se os efeitos do sistema estão habilitados no fluxo de modo compartilhado que flui para ou do dispositivo de ponto de extremidade de áudio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089451"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a><span data-ttu-id="cc4bb-103">PKEY \_ AudioEndpoint \_ Disable \_ SysFx</span><span class="sxs-lookup"><span data-stu-id="cc4bb-103">PKEY\_AudioEndpoint\_Disable\_SysFx</span></span>

<span data-ttu-id="cc4bb-104">A propriedade **PKEY \_ AudioEndpoint \_ Disable \_ SysFx** especifica se os efeitos do sistema estão habilitados no fluxo de modo compartilhado que flui para ou do dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="cc4bb-104">The **PKEY\_AudioEndpoint\_Disable\_SysFx** property specifies whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>

<span data-ttu-id="cc4bb-105">Os efeitos do sistema são implementados como objetos de processamento de áudio (APOs) que podem ser inseridos em um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="cc4bb-105">System effects are implemented as audio processing objects (APOs) that can be inserted into an audio stream.</span></span> <span data-ttu-id="cc4bb-106">APOs são módulos de software que executam funções de processamento de áudio, como controle de volume e conversão de formato.</span><span class="sxs-lookup"><span data-stu-id="cc4bb-106">APOs are software modules that perform audio processing functions such as volume control and format conversion.</span></span> <span data-ttu-id="cc4bb-107">A desabilitação dos efeitos do sistema para um dispositivo de ponto de extremidade permite que o fluxo associado passe pelo APOs não modificado.</span><span class="sxs-lookup"><span data-stu-id="cc4bb-107">Disabling the system effects for an endpoint device enables the associated stream to pass through the APOs unmodified.</span></span>

<span data-ttu-id="cc4bb-108">Para obter mais informações sobre os efeitos do sistema no Windows Vista, consulte os White papers intitulados "efeitos de áudio personalizados no Windows Vista" e "reutilizando os efeitos do sistema de áudio do Windows Vista" no site de [tecnologias do dispositivo de áudio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="cc4bb-108">For more information about system effects in Windows Vista, see the white papers titled "Custom Audio Effects in Windows Vista" and "Reusing Windows Vista Audio System Effects" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="cc4bb-109">Essa propriedade aplica-se somente aos efeitos locais e aos efeitos globais APOs que foram instalados pelo arquivo. inf que instalou o adaptador de áudio ao qual o dispositivo de ponto de extremidade está conectado.</span><span class="sxs-lookup"><span data-stu-id="cc4bb-109">This property applies only to the local-effects and global-effects APOs that were installed by the .inf file that installed the audio adapter to which the endpoint device is connected.</span></span> <span data-ttu-id="cc4bb-110">Além disso, essa propriedade afeta apenas o dispositivo de ponto de extremidade de destino — ele não tem nenhum efeito sobre os efeitos do sistema para nenhum outro dispositivo de ponto de extremidade, mesmo se eles se conectarem ao mesmo adaptador.</span><span class="sxs-lookup"><span data-stu-id="cc4bb-110">In addition, this property affects only the target endpoint device—it has no effect on the system effects for any other endpoint devices, even if they connect to the same adapter.</span></span>

<span data-ttu-id="cc4bb-111">O membro **VT** da estrutura **PROPVARIANT** é definido como **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="cc4bb-111">The **vt** member of the **PROPVARIANT** structure is set to **VT\_UI4**.</span></span>

<span data-ttu-id="cc4bb-112">O membro **ulVal** da estrutura **PROPVARIANT** é definido como **Endpoint \_ SYSFX \_ habilitado** se os efeitos do sistema estiverem habilitados ou o ponto de **extremidade \_ SYSFX \_ desabilitado** se eles estiverem desabilitados.</span><span class="sxs-lookup"><span data-stu-id="cc4bb-112">The **ulVal** member of the **PROPVARIANT** structure is set to **ENDPOINT\_SYSFX\_ENABLED** if system effects are enabled or to **ENDPOINT\_SYSFX\_DISABLED** if they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc4bb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc4bb-113">Requirements</span></span>



| <span data-ttu-id="cc4bb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc4bb-114">Requirement</span></span> | <span data-ttu-id="cc4bb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cc4bb-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4bb-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc4bb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cc4bb-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc4bb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cc4bb-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc4bb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cc4bb-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc4bb-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cc4bb-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc4bb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc4bb-121"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc4bb-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc4bb-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc4bb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc4bb-123">**Propriedades do ponto de extremidade de áudio**</span><span class="sxs-lookup"><span data-stu-id="cc4bb-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="cc4bb-124">Propriedades de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="cc4bb-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




