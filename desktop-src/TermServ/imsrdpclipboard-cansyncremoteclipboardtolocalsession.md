---
title: Método IMsRdpClipboard CanSyncRemoteClipboardToLocalSession
description: Indica se a área de transferência remota pode ser sincronizada com a sessão local.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CanSyncRemoteClipboardToLocalSession
- Método CanSyncRemoteClipboardToLocalSession Serviços de Área de Trabalho Remota, interface IMsRdpClipboard
- Serviços de Área de Trabalho Remota de interface IMsRdpClipboard, método CanSyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105793774"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="011ba-106">Método IMsRdpClipboard:: CanSyncRemoteClipboardToLocalSession</span><span class="sxs-lookup"><span data-stu-id="011ba-106">IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="011ba-107">Indica se a área de transferência remota pode ser sincronizada com a sessão local.</span><span class="sxs-lookup"><span data-stu-id="011ba-107">Indicates whether the remote Clipboard can be synced to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="011ba-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="011ba-108">Syntax</span></span>

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="011ba-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="011ba-109">Parameters</span></span>

<span data-ttu-id="011ba-110">**True** se a área de transferência remota puder ser sincronizada com a sessão local; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="011ba-110">**TRUE** if the remote Clipboard can be synced to the local session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="011ba-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="011ba-111">Return value</span></span>

<span data-ttu-id="011ba-112">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="011ba-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="011ba-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="011ba-113">Requirements</span></span>

| <span data-ttu-id="011ba-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="011ba-114">Requirement</span></span> | <span data-ttu-id="011ba-115">Valor</span><span class="sxs-lookup"><span data-stu-id="011ba-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="011ba-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="011ba-116">Minimum supported client</span></span>| <span data-ttu-id="011ba-117">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="011ba-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="011ba-118">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="011ba-118">Type library</span></span>            | <span data-ttu-id="011ba-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="011ba-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="011ba-120">DLL</span><span class="sxs-lookup"><span data-stu-id="011ba-120">DLL</span></span>                  | <span data-ttu-id="011ba-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="011ba-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="011ba-122">IID</span><span class="sxs-lookup"><span data-stu-id="011ba-122">IID</span></span>                      | <span data-ttu-id="011ba-123">IID \_ IMsRdpClipboard é definido como 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="011ba-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="011ba-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="011ba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011ba-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="011ba-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>