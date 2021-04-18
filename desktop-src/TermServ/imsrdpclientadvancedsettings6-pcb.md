---
title: Propriedade IMsRdpClientAdvancedSettings6 PCB
description: Especifica a configuração de BLOB de preconexão (PCB) a ser usada antes de se conectar para transmissão para o servidor. | Propriedade IMsRdpClientAdvancedSettings6 PCB
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PCB
- Propriedade PCB Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade PCB
- Propriedade PCB Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade PCB
- Propriedade PCB Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade PCB
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da9cfa12ec944ea8f745ec3399c2a53f6b7c6b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756969"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a><span data-ttu-id="389d1-111">IMsRdpClientAdvancedSettings6::P Propriedade CB</span><span class="sxs-lookup"><span data-stu-id="389d1-111">IMsRdpClientAdvancedSettings6::PCB property</span></span>

<span data-ttu-id="389d1-112">Especifica a configuração de BLOB de preconexão (PCB) a ser usada antes de se conectar para transmissão para o servidor.</span><span class="sxs-lookup"><span data-stu-id="389d1-112">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="389d1-113">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="389d1-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="389d1-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="389d1-114">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="389d1-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="389d1-115">Property value</span></span>

<span data-ttu-id="389d1-116">Especifica a configuração de BLOB a ser usada antes da conexão.</span><span class="sxs-lookup"><span data-stu-id="389d1-116">Specifies the BLOB setting to use prior to connecting.</span></span>

## <a name="remarks"></a><span data-ttu-id="389d1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="389d1-117">Remarks</span></span>

<span data-ttu-id="389d1-118">Essa propriedade só tem suporte nos clientes Conexão de Área de Trabalho Remota 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="389d1-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="389d1-119">O servidor usa a configuração de BLOB para identificar o processo de destino para a conexão.</span><span class="sxs-lookup"><span data-stu-id="389d1-119">The server uses the BLOB setting to identify the target process for the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="389d1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="389d1-120">Requirements</span></span>



| <span data-ttu-id="389d1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="389d1-121">Requirement</span></span> | <span data-ttu-id="389d1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="389d1-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="389d1-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="389d1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="389d1-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="389d1-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="389d1-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="389d1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="389d1-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="389d1-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="389d1-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="389d1-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="389d1-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="389d1-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="389d1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="389d1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="389d1-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="389d1-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="389d1-131">IID</span><span class="sxs-lookup"><span data-stu-id="389d1-131">IID</span></span><br/>                      | <span data-ttu-id="389d1-132">IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="389d1-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="389d1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="389d1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="389d1-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="389d1-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="389d1-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="389d1-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="389d1-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="389d1-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





