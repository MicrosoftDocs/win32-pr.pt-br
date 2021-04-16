---
title: Interface IMsRdpClientSecuredSettings2
description: Define propriedades adicionais do controle ActiveX Área de Trabalho Remota que são restritas a zonas de segurança de URL específicas do Internet Explorer.
ms.assetid: dde9824c-7adf-4783-bb1a-fb2bdbb7aead
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings2
- Serviços de Área de Trabalho Remota da interface IMsRdpClientSecuredSettings2, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ceaf322b51a4b619f8d73a898c444706d61f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757600"
---
# <a name="imsrdpclientsecuredsettings2-interface"></a><span data-ttu-id="b0982-105">Interface IMsRdpClientSecuredSettings2</span><span class="sxs-lookup"><span data-stu-id="b0982-105">IMsRdpClientSecuredSettings2 interface</span></span>

<span data-ttu-id="b0982-106">Define propriedades adicionais do controle ActiveX Área de Trabalho Remota que são restritas a zonas de segurança de URL específicas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b0982-106">Defines additional properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="b0982-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b0982-107">Members</span></span>

<span data-ttu-id="b0982-108">A interface **IMsRdpClientSecuredSettings2** herda de [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b0982-108">The **IMsRdpClientSecuredSettings2** interface inherits from [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md).</span></span> <span data-ttu-id="b0982-109">**IMsRdpClientSecuredSettings2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b0982-109">**IMsRdpClientSecuredSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="b0982-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0982-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0982-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0982-111">Properties</span></span>

<span data-ttu-id="b0982-112">A interface **IMsRdpClientSecuredSettings2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0982-112">The **IMsRdpClientSecuredSettings2** interface has these properties.</span></span>



| <span data-ttu-id="b0982-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b0982-113">Property</span></span>                                                   | <span data-ttu-id="b0982-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b0982-114">Access type</span></span>           | <span data-ttu-id="b0982-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0982-115">Description</span></span>                                                                                                          |
|:-----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0982-116">**PCB**</span><span class="sxs-lookup"><span data-stu-id="b0982-116">**PCB**</span></span>](imsrdpclientsecuredsettings2-pcb.md)<br/> | <span data-ttu-id="b0982-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b0982-117">Read/write</span></span><br/> | <span data-ttu-id="b0982-118">Especifica a configuração de BLOB de preconexão (PCB) a ser usada antes de se conectar para transmissão para o servidor.</span><span class="sxs-lookup"><span data-stu-id="b0982-118">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0982-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0982-119">Requirements</span></span>



| <span data-ttu-id="b0982-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0982-120">Requirement</span></span> | <span data-ttu-id="b0982-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b0982-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0982-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0982-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b0982-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b0982-123">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="b0982-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0982-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b0982-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0982-125">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="b0982-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b0982-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="b0982-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0982-127"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="b0982-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b0982-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0982-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0982-129"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="b0982-130">IID</span><span class="sxs-lookup"><span data-stu-id="b0982-130">IID</span></span><br/>                      | <span data-ttu-id="b0982-131">IID \_ IMsRdpClientSecuredSettings é definido como 25f2ce20-8b1d-4971-A7CD-549dae201fc0</span><span class="sxs-lookup"><span data-stu-id="b0982-131">IID\_IMsRdpClientSecuredSettings is defined as 25f2ce20-8b1d-4971-a7cd-549dae201fc0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0982-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0982-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0982-133">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="b0982-133">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





