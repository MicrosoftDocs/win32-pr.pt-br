---
title: EC_WMT_EVENT (SDK do Windows Media Format 11)
description: '\_evento de WMT do EC \_'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- SDK do Windows Media Format, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- DRM (gerenciamento de direitos digitais), EC_WMT_EVENT
- DRM (gerenciamento de direitos digitais), EC_WMT_EVENT
- ASF (Advanced Systems Format), EC_WMT_EVENT
- ASF (formato de sistemas avançados), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454526"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a><span data-ttu-id="80bb6-110">EC_WMT_EVENT (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="80bb6-110">EC_WMT_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="80bb6-111">Enviado pelo Windows Media Format SDK quando um aplicativo usa o filtro de leitor de ASF para reproduzir arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="80bb6-111">Sent by the Windows Media Format SDK when an application uses the ASF Reader filter to play ASF files protected by digital rights management (DRM).</span></span>

<span data-ttu-id="80bb6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80bb6-112">Parameters</span></span>

<span data-ttu-id="80bb6-113">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="80bb6-113">*lParam1*</span></span>

<span data-ttu-id="80bb6-114">Pode ser um dos seguintes valores de \_ status de WMT.</span><span class="sxs-lookup"><span data-stu-id="80bb6-114">Can be one of the following WMT\_STATUS values.</span></span>



| <span data-ttu-id="80bb6-115">Mensagem de status do WMT \_</span><span class="sxs-lookup"><span data-stu-id="80bb6-115">WMT\_STATUS Message</span></span>           | <span data-ttu-id="80bb6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="80bb6-116">Description</span></span>                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bb6-117">WMT \_ sem \_ direitos</span><span class="sxs-lookup"><span data-stu-id="80bb6-117">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="80bb6-118">O arquivo é protegido com o DRM versão 1 e o aplicativo não tem direitos para executar a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="80bb6-118">The file is protected with DRM version 1 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="80bb6-119">\_licença de aquisição do WMT \_</span><span class="sxs-lookup"><span data-stu-id="80bb6-119">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="80bb6-120">O processo de aquisição de licença foi concluído.</span><span class="sxs-lookup"><span data-stu-id="80bb6-120">The license acquisition process has been completed.</span></span> <span data-ttu-id="80bb6-121">(Isso não significa, necessariamente, que uma licença foi adquirida com êxito.)</span><span class="sxs-lookup"><span data-stu-id="80bb6-121">(This does not necessarily mean that a license was successfully acquired.)</span></span> |
| <span data-ttu-id="80bb6-122">WMT \_ sem \_ direitos \_ ex</span><span class="sxs-lookup"><span data-stu-id="80bb6-122">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="80bb6-123">O arquivo é protegido com o DRM versão 7 e o aplicativo não tem direitos para executar a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="80bb6-123">The file is protected with DRM version 7 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="80bb6-124">WMT \_ precisa de \_ individualização</span><span class="sxs-lookup"><span data-stu-id="80bb6-124">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="80bb6-125">A licença permite que somente aplicativos individualizados executem a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="80bb6-125">The license allows only individualized applications to perform the requested action.</span></span>                                           |
| <span data-ttu-id="80bb6-126">\_individualizar WMT</span><span class="sxs-lookup"><span data-stu-id="80bb6-126">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="80bb6-127">O processo de individualização agora está sendo executado ou foi concluído.</span><span class="sxs-lookup"><span data-stu-id="80bb6-127">The individualization process is now being performed or has been completed.</span></span>                                                    |



 

<span data-ttu-id="80bb6-128">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="80bb6-128">*lParam2*</span></span>

<span data-ttu-id="80bb6-129">Ponteiro para uma estrutura de **\_ \_ \_ dados de evento WMT** que contém informações sobre o evento no ponteiro do membro **pData** , bem como um código de status **HRESULT** enviado pelo Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="80bb6-129">Pointer to an **AM\_WMT\_EVENT\_DATA** structure that contains information about the event in the **pData** member pointer, as well as an **HRESULT** status code sent by the Windows Media Format SDK.</span></span> <span data-ttu-id="80bb6-130">O valor de *lParam2* depende do valor de *lParam1*, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="80bb6-130">The value of *lParam2* depends on the value of *lParam1*, as described in the following table.</span></span> <span data-ttu-id="80bb6-131">(As estruturas "WM \_ " são definidas no Windows Media Format SDK.)</span><span class="sxs-lookup"><span data-stu-id="80bb6-131">(The "WM\_" structures are defined in the Windows Media Format SDK.)</span></span>



| <span data-ttu-id="80bb6-132">Se lParam1 for...</span><span class="sxs-lookup"><span data-stu-id="80bb6-132">If lParam1 is...</span></span>              | <span data-ttu-id="80bb6-133">AM \_ WMT \_ Event \_ Data. pData is...</span><span class="sxs-lookup"><span data-stu-id="80bb6-133">AM\_WMT\_EVENT\_DATA.pData is...</span></span>                            |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="80bb6-134">WMT \_ sem \_ direitos</span><span class="sxs-lookup"><span data-stu-id="80bb6-134">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="80bb6-135">Um ponteiro para uma cadeia de caracteres **WCHAR** que contém uma URL de desafio.</span><span class="sxs-lookup"><span data-stu-id="80bb6-135">A pointer to a **WCHAR** string containing a challenge URL.</span></span> |
| <span data-ttu-id="80bb6-136">\_licença de aquisição do WMT \_</span><span class="sxs-lookup"><span data-stu-id="80bb6-136">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="80bb6-137">Um ponteiro para uma estrutura de **\_ \_ \_ dados obter licença do WM** .</span><span class="sxs-lookup"><span data-stu-id="80bb6-137">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="80bb6-138">WMT \_ sem \_ direitos \_ ex</span><span class="sxs-lookup"><span data-stu-id="80bb6-138">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="80bb6-139">Um ponteiro para uma estrutura de **\_ \_ \_ dados obter licença do WM** .</span><span class="sxs-lookup"><span data-stu-id="80bb6-139">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="80bb6-140">WMT \_ precisa de \_ individualização</span><span class="sxs-lookup"><span data-stu-id="80bb6-140">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="80bb6-141">NULL.</span><span class="sxs-lookup"><span data-stu-id="80bb6-141">NULL.</span></span>                                                       |
| <span data-ttu-id="80bb6-142">\_individualizar WMT</span><span class="sxs-lookup"><span data-stu-id="80bb6-142">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="80bb6-143">Um ponteiro para uma estrutura de **\_ \_ status de individualização do WM** .</span><span class="sxs-lookup"><span data-stu-id="80bb6-143">A pointer to a **WM\_INDIVIDUALIZE\_STATUS** structure.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="80bb6-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80bb6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80bb6-145">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="80bb6-145">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="80bb6-146">**Referência do QASF do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="80bb6-146">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="80bb6-147">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="80bb6-147">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




