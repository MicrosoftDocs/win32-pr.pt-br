---
title: Interface IMsRdpClientAdvancedSettings4
description: Gerencia configurações avançadas do cliente. Deriva da interface IMsRdpClientAdvancedSettings3.
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings4, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d840206a139e3c3272551eab6a187a7b18416e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369581"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a><span data-ttu-id="89a39-106">Interface IMsRdpClientAdvancedSettings4</span><span class="sxs-lookup"><span data-stu-id="89a39-106">IMsRdpClientAdvancedSettings4 interface</span></span>

<span data-ttu-id="89a39-107">Gerencia configurações avançadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="89a39-107">Manages advanced client settings.</span></span> <span data-ttu-id="89a39-108">Deriva da interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="89a39-108">Derives from the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="89a39-109">Essa interface inclui métodos para recuperar e definir propriedades avançadas (opcionais) para o controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="89a39-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="89a39-110">Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="89a39-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="89a39-111">Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings4 de IID** para **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="89a39-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings4** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="89a39-112">Membros</span><span class="sxs-lookup"><span data-stu-id="89a39-112">Members</span></span>

<span data-ttu-id="89a39-113">A interface **IMsRdpClientAdvancedSettings4** herda de [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span><span class="sxs-lookup"><span data-stu-id="89a39-113">The **IMsRdpClientAdvancedSettings4** interface inherits from [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span></span> <span data-ttu-id="89a39-114">**IMsRdpClientAdvancedSettings4** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="89a39-114">**IMsRdpClientAdvancedSettings4** also has these types of members:</span></span>

-   [<span data-ttu-id="89a39-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89a39-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89a39-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89a39-116">Properties</span></span>

<span data-ttu-id="89a39-117">A interface **IMsRdpClientAdvancedSettings4** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="89a39-117">The **IMsRdpClientAdvancedSettings4** interface has these properties.</span></span>



| <span data-ttu-id="89a39-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="89a39-118">Property</span></span>                                                                                    | <span data-ttu-id="89a39-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="89a39-119">Access type</span></span>           | <span data-ttu-id="89a39-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="89a39-120">Description</span></span>                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="89a39-121">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="89a39-121">**AuthenticationLevel**</span></span>](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | <span data-ttu-id="89a39-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89a39-122">Read/write</span></span><br/> | <span data-ttu-id="89a39-123">Especifica o nível de autenticação a ser usado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="89a39-123">Specifies the authentication level to use for the connection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89a39-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="89a39-124">Remarks</span></span>

<span data-ttu-id="89a39-125">Essa interface foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="89a39-125">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="89a39-126">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="89a39-126">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="89a39-127">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="89a39-127">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="89a39-128">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="89a39-128">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="89a39-129">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="89a39-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89a39-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89a39-130">Requirements</span></span>



| <span data-ttu-id="89a39-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="89a39-131">Requirement</span></span> | <span data-ttu-id="89a39-132">Valor</span><span class="sxs-lookup"><span data-stu-id="89a39-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a39-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89a39-133">Minimum supported client</span></span><br/> | <span data-ttu-id="89a39-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89a39-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="89a39-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89a39-135">Minimum supported server</span></span><br/> | <span data-ttu-id="89a39-136">Windows Server 2008, Windows Server 2008 com SP1</span><span class="sxs-lookup"><span data-stu-id="89a39-136">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="89a39-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="89a39-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="89a39-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a39-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="89a39-139">DLL</span><span class="sxs-lookup"><span data-stu-id="89a39-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89a39-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a39-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="89a39-141">IID</span><span class="sxs-lookup"><span data-stu-id="89a39-141">IID</span></span><br/>                      | <span data-ttu-id="89a39-142">IID \_ IMsRdpClientAdvancedSettings4 é definido como FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="89a39-142">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89a39-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="89a39-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a39-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="89a39-144">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="89a39-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="89a39-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="89a39-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="89a39-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="89a39-147">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="89a39-147">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="89a39-148">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="89a39-148">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

