---
title: Interface do IMsRdpClipboard
description: Representa o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClipboard
- Serviços de Área de Trabalho Remota da interface IMsRdpClipboard, descrita
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104087199"
---
# <a name="imsrdpclipboard-interface"></a><span data-ttu-id="59c79-105">Interface do IMsRdpClipboard</span><span class="sxs-lookup"><span data-stu-id="59c79-105">IMsRdpClipboard interface</span></span>

<span data-ttu-id="59c79-106">Representa o controlador da área de transferência usado para sincronizar as áreas de transferência locais e remotas se a sincronização da área de transferência manual estiver habilitada (ou seja, o valor da propriedade [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) for definido como **true**).</span><span class="sxs-lookup"><span data-stu-id="59c79-106">Represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="members"></a><span data-ttu-id="59c79-107">Membros</span><span class="sxs-lookup"><span data-stu-id="59c79-107">Members</span></span>

<span data-ttu-id="59c79-108">A interface **IMsRdpClipboard** herda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="59c79-108">The **IMsRdpClipboard** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="59c79-109">**IMsRdpClipboard** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="59c79-109">**IMsRdpClipboard** also has these types of members:</span></span>

- [<span data-ttu-id="59c79-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="59c79-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="59c79-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="59c79-111">Methods</span></span>

<span data-ttu-id="59c79-112">A interface **IMsRdpClipboard** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="59c79-112">The **IMsRdpClipboard** interface has these methods.</span></span>


| <span data-ttu-id="59c79-113">Método</span><span class="sxs-lookup"><span data-stu-id="59c79-113">Method</span></span>        | <span data-ttu-id="59c79-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="59c79-114">Description</span></span>      |
|:---------------|:----------------|
| [<span data-ttu-id="59c79-115">**CanSyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="59c79-115">**CanSyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  <span data-ttu-id="59c79-116">Indica se a área de transferência local pode ser sincronizada com a sessão remota.</span><span class="sxs-lookup"><span data-stu-id="59c79-116">Indicates whether the local Clipboard can be synced to the remote session.</span></span>                   |
| [<span data-ttu-id="59c79-117">**CanSyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="59c79-117">**CanSyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  <span data-ttu-id="59c79-118">Indica se a área de transferência remota pode ser sincronizada com a sessão local.</span><span class="sxs-lookup"><span data-stu-id="59c79-118">Indicates whether the remote Clipboard can be synced to the local session.</span></span>                   |
| [<span data-ttu-id="59c79-119">**SyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="59c79-119">**SyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  <span data-ttu-id="59c79-120">Sincroniza a área de transferência local com a sessão remota.</span><span class="sxs-lookup"><span data-stu-id="59c79-120">Syncs the local Clipboard to the remote session.</span></span>                   |
| [<span data-ttu-id="59c79-121">**SyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="59c79-121">**SyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   <span data-ttu-id="59c79-122">Sincroniza a área de transferência remota para a sessão local.</span><span class="sxs-lookup"><span data-stu-id="59c79-122">Syncs the remote Clipboard to the local session.</span></span>                      |

## <a name="requirements"></a><span data-ttu-id="59c79-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59c79-123">Requirements</span></span>

| <span data-ttu-id="59c79-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c79-124">Requirement</span></span> | <span data-ttu-id="59c79-125">Valor</span><span class="sxs-lookup"><span data-stu-id="59c79-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="59c79-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59c79-126">Minimum supported client</span></span>| <span data-ttu-id="59c79-127">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="59c79-127">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="59c79-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="59c79-128">Type library</span></span>            | <span data-ttu-id="59c79-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="59c79-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="59c79-130">DLL</span><span class="sxs-lookup"><span data-stu-id="59c79-130">DLL</span></span>                  | <span data-ttu-id="59c79-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="59c79-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="59c79-132">IID</span><span class="sxs-lookup"><span data-stu-id="59c79-132">IID</span></span>                      | <span data-ttu-id="59c79-133">IID \_ IMsRdpClipboard é definido como 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="59c79-133">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>            |

## <a name="see-also"></a><span data-ttu-id="59c79-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="59c79-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c79-135">**IMsRdpClientNonScriptable7:: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="59c79-135">**IMsRdpClientNonScriptable7::Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
