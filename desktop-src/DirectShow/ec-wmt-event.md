---
description: Enviado pelo filtro de leitor ASF do WM quando ele lê arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752678"
---
# <a name="ec_wmt_event-dshowh"></a><span data-ttu-id="ae818-103">EC_WMT_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="ae818-103">EC_WMT_EVENT (Dshow.h)</span></span>

<span data-ttu-id="ae818-104">Enviado pelo filtro de [leitor ASF do WM](wm-asf-reader-filter.md) quando ele lê arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="ae818-104">Sent by the [WM ASF Reader](wm-asf-reader-filter.md) filter when it reads ASF files protected by digital rights management (DRM).</span></span>

## <a name="parameters"></a><span data-ttu-id="ae818-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae818-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae818-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ae818-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ae818-107">Um dos seguintes valores **de \_ status de WMT** :</span><span class="sxs-lookup"><span data-stu-id="ae818-107">One of the following **WMT\_STATUS** values:</span></span>



| <span data-ttu-id="ae818-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ae818-108">Value</span></span>                         | <span data-ttu-id="ae818-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae818-109">Description</span></span>                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae818-110">\_licença de aquisição do WMT \_</span><span class="sxs-lookup"><span data-stu-id="ae818-110">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="ae818-111">Enviado quando o componente DRM concluiu o processo de aquisição de licença, seja com êxito ou sem êxito.</span><span class="sxs-lookup"><span data-stu-id="ae818-111">Sent when the DRM component has completed the license acquisition process, either successfully or unsuccessfully.</span></span> |
| <span data-ttu-id="ae818-112">\_individualizar WMT</span><span class="sxs-lookup"><span data-stu-id="ae818-112">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="ae818-113">O processo de atualização de segurança foi concluído com êxito ou não.</span><span class="sxs-lookup"><span data-stu-id="ae818-113">The security upgrade process has completed, either successfully or unsuccessfully.</span></span>                                |
| <span data-ttu-id="ae818-114">WMT \_ precisa de \_ individualização</span><span class="sxs-lookup"><span data-stu-id="ae818-114">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="ae818-115">O arquivo requer que um aplicativo receba uma atualização de segurança antes de executar a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="ae818-115">The file requires that an application receive a security upgrade before performing the requested action.</span></span>          |
| <span data-ttu-id="ae818-116">WMT \_ sem \_ direitos</span><span class="sxs-lookup"><span data-stu-id="ae818-116">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="ae818-117">O aplicativo não tem direitos para executar a ação solicitada em um arquivo protegido pelo DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="ae818-117">The application has no rights to perform he requested action on a file protected by DRM version 1.</span></span>                |
| <span data-ttu-id="ae818-118">WMT \_ sem \_ direitos \_ ex</span><span class="sxs-lookup"><span data-stu-id="ae818-118">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="ae818-119">O aplicativo não tem direitos para executar a ação solicitada em um arquivo protegido pelo DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="ae818-119">The application has no rights to perform he requested action on a file protected by DRM version 7.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="ae818-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ae818-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ae818-121">Ponteiro para uma estrutura de [**\_ \_ \_ dados de evento WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que contém informações sobre o evento ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ae818-121">Pointer to an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) structure that contains information about the event, or **NULL**.</span></span> <span data-ttu-id="ae818-122">O membro **pData** dessa estrutura aponta para dados adicionais, cujo tipo depende do valor de **lParam1**, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae818-122">The **pData** member of this structure points to additional data, whose type depends on the value of **lParam1**, as shown in the following table.</span></span>



| <span data-ttu-id="ae818-123">lParam1</span><span class="sxs-lookup"><span data-stu-id="ae818-123">lParam1</span></span>                       | <span data-ttu-id="ae818-124">\_WMT \_ dados de evento am \_ . pData</span><span class="sxs-lookup"><span data-stu-id="ae818-124">AM\_WMT\_EVENT\_DATA.pData</span></span>                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae818-125">\_licença de aquisição do WMT \_</span><span class="sxs-lookup"><span data-stu-id="ae818-125">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="ae818-126">Ponteiro para uma estrutura de [**\_ \_ \_ dados obter licença do WM**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="ae818-126">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span> <span data-ttu-id="ae818-127">Essa estrutura está documentada no Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="ae818-127">This structure is documented in the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="ae818-128">\_individualizar WMT</span><span class="sxs-lookup"><span data-stu-id="ae818-128">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="ae818-129">Ponteiro para uma estrutura de [**\_ \_ status de individualização do WM**](/windows/desktop/wmformat/wm-individualize-status) .</span><span class="sxs-lookup"><span data-stu-id="ae818-129">Pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](/windows/desktop/wmformat/wm-individualize-status) structure.</span></span>                                                        |
| <span data-ttu-id="ae818-130">WMT \_ precisa de \_ individualização</span><span class="sxs-lookup"><span data-stu-id="ae818-130">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="ae818-131">**NULL**.</span><span class="sxs-lookup"><span data-stu-id="ae818-131">**NULL**.</span></span>                                                                                                                                        |
| <span data-ttu-id="ae818-132">WMT \_ sem \_ direitos</span><span class="sxs-lookup"><span data-stu-id="ae818-132">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="ae818-133">Ponteiro para uma cadeia de caracteres largos contendo uma URL de desafio.</span><span class="sxs-lookup"><span data-stu-id="ae818-133">Pointer to a wide-character string containing a challenge URL.</span></span>                                                                                   |
| <span data-ttu-id="ae818-134">WMT \_ sem \_ direitos \_ ex</span><span class="sxs-lookup"><span data-stu-id="ae818-134">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="ae818-135">Ponteiro para uma estrutura de [**\_ \_ \_ dados obter licença do WM**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="ae818-135">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span>                                                               |



 

<span data-ttu-id="ae818-136">O valor de *lParam2* pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ae818-136">The value of *lParam2* might be **NULL**.</span></span> <span data-ttu-id="ae818-137">Verifique o valor antes de cancelar a referência ao ponteiro.</span><span class="sxs-lookup"><span data-stu-id="ae818-137">Check the value before dereferencing the pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae818-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae818-138">Remarks</span></span>

<span data-ttu-id="ae818-139">Consulte a documentação do SDK do Windows Media Format para obter mais informações sobre como habilitar a reprodução de arquivos protegidos por DRM.</span><span class="sxs-lookup"><span data-stu-id="ae818-139">See the Windows Media Format SDK documentation for more information on enabling playback of DRM-protected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae818-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae818-140">Requirements</span></span>



| <span data-ttu-id="ae818-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae818-141">Requirement</span></span> | <span data-ttu-id="ae818-142">Valor</span><span class="sxs-lookup"><span data-stu-id="ae818-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae818-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae818-143">Header</span></span><br/> | <dl> <span data-ttu-id="ae818-144"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae818-144"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae818-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae818-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae818-146">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="ae818-146">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ae818-147">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="ae818-147">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

