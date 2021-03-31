---
title: Enumeração VMEndpointType (VPCCOMInterfaces. h)
description: Especifica o tipo de ponto de extremidade.
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- VMEndpointType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912eb43147af03dd2b9923c4bdb778044f40d023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824376"
---
# <a name="vmendpointtype-enumeration"></a><span data-ttu-id="f7a44-104">Enumeração VMEndpointType</span><span class="sxs-lookup"><span data-stu-id="f7a44-104">VMEndpointType enumeration</span></span>

<span data-ttu-id="f7a44-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f7a44-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f7a44-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f7a44-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f7a44-107">Especifica o tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f7a44-107">Specifies the endpoint type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a44-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7a44-108">Syntax</span></span>


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a><span data-ttu-id="f7a44-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="f7a44-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f7a44-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint \_ NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="f7a44-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="f7a44-111">O lado do host.</span><span class="sxs-lookup"><span data-stu-id="f7a44-111">The host side.</span></span>

</dd> <dt>

<span data-ttu-id="f7a44-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**\_tcpip vmEndpoint**</span><span class="sxs-lookup"><span data-stu-id="f7a44-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint\_TCPIP**</span></span>
</dt> <dd>

<span data-ttu-id="f7a44-113">O lado do convidado.</span><span class="sxs-lookup"><span data-stu-id="f7a44-113">The guest side.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7a44-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7a44-114">Requirements</span></span>



| <span data-ttu-id="f7a44-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7a44-115">Requirement</span></span> | <span data-ttu-id="f7a44-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f7a44-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a44-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7a44-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f7a44-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f7a44-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7a44-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7a44-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f7a44-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f7a44-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f7a44-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f7a44-121">End of client support</span></span><br/>    | <span data-ttu-id="f7a44-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f7a44-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f7a44-123">Produto</span><span class="sxs-lookup"><span data-stu-id="f7a44-123">Product</span></span><br/>                  | <span data-ttu-id="f7a44-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f7a44-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f7a44-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7a44-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7a44-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7a44-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7a44-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f7a44-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a44-128">**IVMVirtualMachine::StartCommunicationChannel**</span><span class="sxs-lookup"><span data-stu-id="f7a44-128">**IVMVirtualMachine::StartCommunicationChannel**</span></span>](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

