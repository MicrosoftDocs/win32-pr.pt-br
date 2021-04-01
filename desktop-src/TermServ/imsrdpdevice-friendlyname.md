---
title: Propriedade FriendlyName IMsRdpDevice
description: Recupera o nome de exibição do dispositivo.
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- Propriedade FriendlyName Serviços de Área de Trabalho Remota
- Propriedade FriendlyName Serviços de Área de Trabalho Remota, interface IMsRdpDevice
- Interface IMsRdpDevice Serviços de Área de Trabalho Remota, Propriedade FriendlyName
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf7963cf49945b886d72a622b517438e24d148f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644410"
---
# <a name="imsrdpdevicefriendlyname-property"></a><span data-ttu-id="4e502-106">Propriedade IMsRdpDevice:: FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4e502-106">IMsRdpDevice::FriendlyName property</span></span>

<span data-ttu-id="4e502-107">Recupera o nome de exibição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e502-107">Retrieves the display name for the device.</span></span>

<span data-ttu-id="4e502-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4e502-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e502-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e502-109">Syntax</span></span>


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a><span data-ttu-id="4e502-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4e502-110">Property value</span></span>

<span data-ttu-id="4e502-111">O nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="4e502-111">The display name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e502-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4e502-112">Error codes</span></span>

<span data-ttu-id="4e502-113">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="4e502-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="4e502-114">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="4e502-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e502-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e502-115">Requirements</span></span>



| <span data-ttu-id="4e502-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e502-116">Requirement</span></span> | <span data-ttu-id="4e502-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4e502-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e502-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e502-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4e502-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e502-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4e502-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e502-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4e502-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e502-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4e502-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4e502-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e502-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e502-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4e502-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4e502-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e502-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e502-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4e502-126">IID</span><span class="sxs-lookup"><span data-stu-id="4e502-126">IID</span></span><br/>                      | <span data-ttu-id="4e502-127">IID \_ IMsRdpDevice é definido como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="4e502-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="4e502-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e502-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e502-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="4e502-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





