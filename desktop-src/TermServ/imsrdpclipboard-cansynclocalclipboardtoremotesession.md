---
title: Método IMsRdpClipboard CanSyncLocalClipboardToRemoteSession
description: Indica se a área de transferência local pode ser sincronizada com a sessão remota.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CanSyncLocalClipboardToRemoteSession
- Método CanSyncLocalClipboardToRemoteSession Serviços de Área de Trabalho Remota, interface IMsRdpClipboard
- Serviços de Área de Trabalho Remota de interface IMsRdpClipboard, método CanSyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105762241"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a><span data-ttu-id="fa16d-106">Método IMsRdpClipboard:: CanSyncLocalClipboardToRemoteSession</span><span class="sxs-lookup"><span data-stu-id="fa16d-106">IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession method</span></span>

<span data-ttu-id="fa16d-107">Indica se a área de transferência local pode ser sincronizada com a sessão remota.</span><span class="sxs-lookup"><span data-stu-id="fa16d-107">Indicates whether the local Clipboard can be synced to the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa16d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa16d-108">Syntax</span></span>

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="fa16d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa16d-109">Parameters</span></span>

<span data-ttu-id="fa16d-110">**True** se a área de transferência local puder ser sincronizada com a sessão remota; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fa16d-110">**TRUE** if the local Clipboard can be synced to the remote session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa16d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa16d-111">Return value</span></span>

<span data-ttu-id="fa16d-112">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fa16d-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa16d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa16d-113">Requirements</span></span>

| <span data-ttu-id="fa16d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa16d-114">Requirement</span></span> | <span data-ttu-id="fa16d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fa16d-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="fa16d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa16d-116">Minimum supported client</span></span>| <span data-ttu-id="fa16d-117">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="fa16d-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="fa16d-118">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fa16d-118">Type library</span></span>            | <span data-ttu-id="fa16d-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fa16d-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="fa16d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fa16d-120">DLL</span></span>                  | <span data-ttu-id="fa16d-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fa16d-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="fa16d-122">IID</span><span class="sxs-lookup"><span data-stu-id="fa16d-122">IID</span></span>                      | <span data-ttu-id="fa16d-123">IID \_ IMsRdpClipboard é definido como 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="fa16d-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="fa16d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa16d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa16d-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="fa16d-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>