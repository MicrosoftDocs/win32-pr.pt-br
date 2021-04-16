---
title: Mensagem de MM_MIXM_CONTROL_CHANGE (mmsystem. h)
description: A \_ mensagem de alteração do controle MIXM mm \_ \_ é enviada por um dispositivo de mixer para notificar um aplicativo de que o estado de um controle associado a uma linha de áudio foi alterado. O aplicativo deve atualizar seus valores de exibição e armazenados em cache para o controle especificado.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- Multimídia do Windows de mensagem MM_MIXM_CONTROL_CHANGE
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750583"
---
# <a name="mm_mixm_control_change-message"></a><span data-ttu-id="45c23-105">MM \_ MIXM \_ controle de \_ alteração de mensagem</span><span class="sxs-lookup"><span data-stu-id="45c23-105">MM\_MIXM\_CONTROL\_CHANGE message</span></span>

<span data-ttu-id="45c23-106">A mensagem de **\_ \_ \_ alteração do controle MIXM mm** é enviada por um dispositivo de mixer para notificar um aplicativo de que o estado de um controle associado a uma linha de áudio foi alterado.</span><span class="sxs-lookup"><span data-stu-id="45c23-106">The **MM\_MIXM\_CONTROL\_CHANGE** message is sent by a mixer device to notify an application that the state of a control associated with an audio line has changed.</span></span> <span data-ttu-id="45c23-107">O aplicativo deve atualizar seus valores de exibição e armazenados em cache para o controle especificado.</span><span class="sxs-lookup"><span data-stu-id="45c23-107">The application should refresh its display and cached values for the specified control.</span></span>


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a><span data-ttu-id="45c23-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45c23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c23-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="45c23-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="45c23-110">Identificador para o dispositivo de mixer (**HMIXER**) que enviou a mensagem de notificação.</span><span class="sxs-lookup"><span data-stu-id="45c23-110">Handle to the mixer device (**HMIXER**) that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="45c23-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span><span class="sxs-lookup"><span data-stu-id="45c23-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span></span>
</dt> <dd>

<span data-ttu-id="45c23-112">Identificador de controle para o controle do mixer que alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="45c23-112">Control identifier for the mixer control that has changed state.</span></span> <span data-ttu-id="45c23-113">Esse identificador é o mesmo que o membro **dwControlID** da estrutura **MIXERCONTROL** retornada pela função **mixerGetLineControls**.</span><span class="sxs-lookup"><span data-stu-id="45c23-113">This identifier is the same as the **dwControlID** member of the **MIXERCONTROL** structure returned by the **mixerGetLineControls** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45c23-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="45c23-114">Remarks</span></span>

<span data-ttu-id="45c23-115">Um aplicativo deve abrir um dispositivo de mixer e especificar uma janela de retorno de chamada para receber a mensagem de **\_ \_ \_ alteração do controle MIXM mm** .</span><span class="sxs-lookup"><span data-stu-id="45c23-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_CONTROL\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c23-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45c23-116">Requirements</span></span>



| <span data-ttu-id="45c23-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="45c23-117">Requirement</span></span> | <span data-ttu-id="45c23-118">Valor</span><span class="sxs-lookup"><span data-stu-id="45c23-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c23-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45c23-119">Minimum supported client</span></span><br/> | <span data-ttu-id="45c23-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45c23-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="45c23-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45c23-121">Minimum supported server</span></span><br/> | <span data-ttu-id="45c23-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45c23-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="45c23-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45c23-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="45c23-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45c23-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45c23-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="45c23-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c23-126">Mixers de áudio</span><span class="sxs-lookup"><span data-stu-id="45c23-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="45c23-127">Mensagens do mixer de áudio</span><span class="sxs-lookup"><span data-stu-id="45c23-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





