---
title: Propriedade IMsRdpClientSecuredSettings2 PCB
description: Especifica a configuração de BLOB de preconexão (PCB) a ser usada antes de se conectar para transmissão para o servidor. | Propriedade IMsRdpClientSecuredSettings2 PCB
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PCB
- Propriedade PCB Serviços de Área de Trabalho Remota, interface IMsRdpClientSecuredSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings2, Propriedade PCB
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105780574"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a><span data-ttu-id="e0139-107">IMsRdpClientSecuredSettings2::P Propriedade CB</span><span class="sxs-lookup"><span data-stu-id="e0139-107">IMsRdpClientSecuredSettings2::PCB property</span></span>

<span data-ttu-id="e0139-108">Especifica a configuração de BLOB de preconexão (PCB) a ser usada antes de se conectar para transmissão para o servidor.</span><span class="sxs-lookup"><span data-stu-id="e0139-108">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="e0139-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e0139-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0139-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0139-110">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="e0139-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e0139-111">Property value</span></span>

<span data-ttu-id="e0139-112">A configuração PCB.</span><span class="sxs-lookup"><span data-stu-id="e0139-112">The PCB setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0139-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0139-113">Requirements</span></span>



| <span data-ttu-id="e0139-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0139-114">Requirement</span></span> | <span data-ttu-id="e0139-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e0139-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0139-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0139-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e0139-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0139-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="e0139-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0139-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e0139-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0139-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e0139-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e0139-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0139-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0139-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0139-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e0139-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0139-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0139-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0139-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0139-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0139-125">**IMsRdpClientSecuredSettings2**</span><span class="sxs-lookup"><span data-stu-id="e0139-125">**IMsRdpClientSecuredSettings2**</span></span>](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





