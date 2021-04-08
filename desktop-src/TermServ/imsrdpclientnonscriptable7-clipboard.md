---
title: Propriedade IMsRdpClientNonScriptable7 Clipboard
description: Obtém o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade da área de transferência
- Propriedade da área de transferência Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable7, Propriedade Clipboard
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103919670"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a><span data-ttu-id="d3456-106">Propriedade IMsRdpClientNonScriptable7:: Clipboard</span><span class="sxs-lookup"><span data-stu-id="d3456-106">IMsRdpClientNonScriptable7::Clipboard property</span></span>

<span data-ttu-id="d3456-107">Obtém o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="d3456-107">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>

<span data-ttu-id="d3456-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d3456-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3456-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3456-109">Syntax</span></span>

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a><span data-ttu-id="d3456-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d3456-110">Property value</span></span>

<span data-ttu-id="d3456-111">Um [IMsRdpClipboard](imsrdpclipboard.md) que representa o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada (ou seja, o valor da propriedade [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) for definido como **true**).</span><span class="sxs-lookup"><span data-stu-id="d3456-111">An [IMsRdpClipboard](imsrdpclipboard.md) that represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3456-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3456-112">Requirements</span></span>

| <span data-ttu-id="d3456-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3456-113">Requirement</span></span> | <span data-ttu-id="d3456-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d3456-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="d3456-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3456-115">Minimum supported client</span></span>| <span data-ttu-id="d3456-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="d3456-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="d3456-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d3456-117">Type library</span></span>            | <span data-ttu-id="d3456-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d3456-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="d3456-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d3456-119">DLL</span></span>                  | <span data-ttu-id="d3456-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d3456-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="d3456-121">IID</span><span class="sxs-lookup"><span data-stu-id="d3456-121">IID</span></span>                      | <span data-ttu-id="d3456-122">IID \_ IMsRdpClientNonScriptable7 é definido como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="d3456-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="d3456-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3456-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3456-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="d3456-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>