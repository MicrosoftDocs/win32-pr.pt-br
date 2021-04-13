---
description: As \_ constantes AUDCLNT SESSIONFLAGS \_ xxx indicam as características de uma sessão de áudio associada ao fluxo.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: Constantes de AUDCLNT_SESSIONFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457175"
---
# <a name="audclnt_sessionflags_xxx-constants"></a><span data-ttu-id="84692-103">\_Constantes AUDCLNT SESSIONFLAGS \_ xxx</span><span class="sxs-lookup"><span data-stu-id="84692-103">AUDCLNT\_SESSIONFLAGS\_XXX Constants</span></span>

<span data-ttu-id="84692-104">As \_ constantes AUDCLNT SESSIONFLAGS \_ xxx indicam as características de uma sessão de áudio associada ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="84692-104">The AUDCLNT\_SESSIONFLAGS\_XXX constants indicate characteristics of an audio session associated with the stream.</span></span> <span data-ttu-id="84692-105">Um cliente pode especificar essas opções durante a inicialização do fluxo por meio do parâmetro *StreamFlags* do método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="84692-105">A client can specify these options during the initialization of the stream by through the *StreamFlags* parameter of the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span>



| <span data-ttu-id="84692-106">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="84692-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="84692-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="84692-107">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <span data-ttu-id="84692-108"><dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="84692-108"><dt>**AUDCLNT\_SESSIONFLAGS\_EXPIREWHENUNOWNED**</dt> <dt>0x10000000 </dt></span></span> </dl>                       | <span data-ttu-id="84692-109">A sessão expira quando não há fluxos associados e proprietário de objetos de controle de sessão que contêm referências.</span><span class="sxs-lookup"><span data-stu-id="84692-109">The session expires when there are no associated streams and owning session control objects holding references.</span></span><br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <span data-ttu-id="84692-110"><dt>**AUDCLNT \_ SESSIONFLAGS \_ Exibir \_ ocultar**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="84692-110"><dt>**AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDE**</dt> <dt>0x20000000 </dt></span></span> </dl>                                     | <span data-ttu-id="84692-111">O controle de volume fica oculto na interface do usuário do mixer de volume quando a sessão de áudio é criada.</span><span class="sxs-lookup"><span data-stu-id="84692-111">The volume control is hidden in the volume mixer user interface when the audio session is created.</span></span> <span data-ttu-id="84692-112">Se a sessão associada ao fluxo já existir antes de [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) abrir o fluxo, o controle de volume será exibido no mixer de volume.</span><span class="sxs-lookup"><span data-stu-id="84692-112">If the session associated with the stream already exists before [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) opens the stream, the volume control is displayed in the volume mixer.</span></span><br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <span data-ttu-id="84692-113"><dt> **AUDCLNT \_ SESSIONFLAGS \_ exibição \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="84692-113"><dt> **AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDEWHENEXPIRED**</dt> <dt>0x40000000 </dt></span></span> </dl> | <span data-ttu-id="84692-114">O controle de volume fica oculto na interface do usuário do mixer de volume depois que a sessão expira.</span><span class="sxs-lookup"><span data-stu-id="84692-114">The volume control is hidden in the volume mixer user interface after the session expires.</span></span> <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="84692-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84692-115">Requirements</span></span>



| <span data-ttu-id="84692-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="84692-116">Requirement</span></span> | <span data-ttu-id="84692-117">Valor</span><span class="sxs-lookup"><span data-stu-id="84692-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84692-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84692-118">Minimum supported client</span></span><br/> | <span data-ttu-id="84692-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="84692-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="84692-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84692-120">Minimum supported server</span></span><br/> | <span data-ttu-id="84692-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="84692-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84692-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84692-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="84692-123"><dt>Audiosessiontypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="84692-123"><dt>Audiosessiontypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84692-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="84692-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84692-125">Principais constantes de áudio</span><span class="sxs-lookup"><span data-stu-id="84692-125">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="84692-126">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="84692-126">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




