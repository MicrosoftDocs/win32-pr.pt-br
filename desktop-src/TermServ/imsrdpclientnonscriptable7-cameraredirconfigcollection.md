---
title: Propriedade IMsRdpClientNonScriptable7 CameraRedirConfigCollection
description: Obtém a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade CameraRedirConfigCollection
- Propriedade CameraRedirConfigCollection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable7, Propriedade CameraRedirConfigCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104295928"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a><span data-ttu-id="f1b33-106">Propriedade IMsRdpClientNonScriptable7:: CameraRedirConfigCollection</span><span class="sxs-lookup"><span data-stu-id="f1b33-106">IMsRdpClientNonScriptable7::CameraRedirConfigCollection property</span></span>

<span data-ttu-id="f1b33-107">Obtém a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="f1b33-107">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

<span data-ttu-id="f1b33-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f1b33-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b33-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1b33-109">Syntax</span></span>


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a><span data-ttu-id="f1b33-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f1b33-110">Property value</span></span>

<span data-ttu-id="f1b33-111">Um [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) que representa a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="f1b33-111">An [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) that represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b33-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1b33-112">Requirements</span></span>

| <span data-ttu-id="f1b33-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1b33-113">Requirement</span></span> | <span data-ttu-id="f1b33-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f1b33-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f1b33-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1b33-115">Minimum supported client</span></span>| <span data-ttu-id="f1b33-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="f1b33-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f1b33-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f1b33-117">Type library</span></span>            | <span data-ttu-id="f1b33-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f1b33-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f1b33-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f1b33-119">DLL</span></span>                  | <span data-ttu-id="f1b33-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f1b33-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f1b33-121">IID</span><span class="sxs-lookup"><span data-stu-id="f1b33-121">IID</span></span>                      | <span data-ttu-id="f1b33-122">IID \_ IMsRdpClientNonScriptable7 é definido como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="f1b33-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="f1b33-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1b33-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b33-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="f1b33-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>