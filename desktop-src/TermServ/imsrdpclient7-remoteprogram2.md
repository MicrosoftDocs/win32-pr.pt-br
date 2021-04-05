---
title: Propriedade IMsRdpClient7 RemoteProgram2
description: Recupera um objeto que dá suporte à interface ITSRemoteProgram2.
ms.assetid: fabdc933-c941-487f-9e49-c20a39e0c86e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RemoteProgram2
- Propriedade RemoteProgram2 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade RemoteProgram2
- Propriedade RemoteProgram2 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade RemoteProgram2
- Propriedade RemoteProgram2 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade RemoteProgram2
- Propriedade RemoteProgram2 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade RemoteProgram2
topic_type:
- apiref
api_name:
- IMsRdpClient7.RemoteProgram2
- IMsRdpClient7.get_RemoteProgram2
- IMsRdpClient8.RemoteProgram2
- IMsRdpClient8.get_RemoteProgram2
- IMsRdpClient9.RemoteProgram2
- IMsRdpClient9.get_RemoteProgram2
- IMsRdpClient10.RemoteProgram2
- IMsRdpClient10.get_RemoteProgram2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1572aada1384a7edfe88b198826050927ae3cff5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918136"
---
# <a name="imsrdpclient7remoteprogram2-property"></a><span data-ttu-id="79e3b-112">Propriedade IMsRdpClient7:: RemoteProgram2</span><span class="sxs-lookup"><span data-stu-id="79e3b-112">IMsRdpClient7::RemoteProgram2 property</span></span>

<span data-ttu-id="79e3b-113">Recupera um objeto que dá suporte à interface [**ITSRemoteProgram2**](itsremoteprogram2.md) .</span><span class="sxs-lookup"><span data-stu-id="79e3b-113">Retrieves an object that supports the [**ITSRemoteProgram2**](itsremoteprogram2.md) interface.</span></span>

<span data-ttu-id="79e3b-114">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="79e3b-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e3b-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79e3b-115">Syntax</span></span>


```C++
HRESULT get_RemoteProgram2(
  [out, retval] ITSRemoteProgram2 **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="79e3b-116">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="79e3b-116">Property value</span></span>

<span data-ttu-id="79e3b-117">O endereço de um ponteiro de interface [**ITSRemoteProgram2**](itsremoteprogram2.md) que recebe o objeto.</span><span class="sxs-lookup"><span data-stu-id="79e3b-117">The address of an [**ITSRemoteProgram2**](itsremoteprogram2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="79e3b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79e3b-118">Requirements</span></span>



| <span data-ttu-id="79e3b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e3b-119">Requirement</span></span> | <span data-ttu-id="79e3b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="79e3b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79e3b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79e3b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="79e3b-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79e3b-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="79e3b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79e3b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="79e3b-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="79e3b-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="79e3b-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="79e3b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="79e3b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e3b-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="79e3b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="79e3b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79e3b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e3b-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="79e3b-129">IID</span><span class="sxs-lookup"><span data-stu-id="79e3b-129">IID</span></span><br/>                      | <span data-ttu-id="79e3b-130">IID \_ IMsRdpClient7 é definido como b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="79e3b-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="79e3b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="79e3b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e3b-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="79e3b-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="79e3b-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="79e3b-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="79e3b-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="79e3b-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="79e3b-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="79e3b-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





