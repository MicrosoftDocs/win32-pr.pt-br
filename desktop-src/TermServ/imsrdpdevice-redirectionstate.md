---
title: Propriedade de redirecionamento IMsRdpDevice
description: Indica o estado de redirecionamento do dispositivo.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- Propriedade redirectionstate Serviços de Área de Trabalho Remota
- Propriedade redirectionstate Serviços de Área de Trabalho Remota, interface IMsRdpDevice
- Serviços de Área de Trabalho Remota de interface IMsRdpDevice, Propriedade redirectionstate
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0f6fb5781700daa8a65443d2713253e97f73bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455058"
---
# <a name="imsrdpdeviceredirectionstate-property"></a><span data-ttu-id="900c2-106">Propriedade IMsRdpDevice:: redirectionstate</span><span class="sxs-lookup"><span data-stu-id="900c2-106">IMsRdpDevice::RedirectionState property</span></span>

<span data-ttu-id="900c2-107">Indica o estado de redirecionamento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="900c2-107">Indicates the redirection state of the device.</span></span>

<span data-ttu-id="900c2-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="900c2-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="900c2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="900c2-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="900c2-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="900c2-110">Property value</span></span>

<span data-ttu-id="900c2-111">Defina esse parâmetro como **Variant \_ false** para desabilitar o redirecionamento ou a **variante \_ true** para habilitar o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="900c2-111">Set this parameter to **VARIANT\_FALSE** to disable redirection or **VARIANT\_TRUE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="900c2-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="900c2-112">Error codes</span></span>

<span data-ttu-id="900c2-113">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="900c2-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="900c2-114">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="900c2-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="900c2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="900c2-115">Requirements</span></span>



| <span data-ttu-id="900c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="900c2-116">Requirement</span></span> | <span data-ttu-id="900c2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="900c2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="900c2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="900c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="900c2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="900c2-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="900c2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="900c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="900c2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="900c2-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="900c2-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="900c2-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="900c2-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="900c2-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="900c2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="900c2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="900c2-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="900c2-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="900c2-126">IID</span><span class="sxs-lookup"><span data-stu-id="900c2-126">IID</span></span><br/>                      | <span data-ttu-id="900c2-127">IID \_ IMsRdpDevice é definido como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="900c2-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="900c2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="900c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900c2-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="900c2-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





