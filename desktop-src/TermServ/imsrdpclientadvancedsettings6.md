---
title: Interface IMsRdpClientAdvancedSettings6
description: Expõe as propriedades que gerenciam as configurações avançadas do controle ActiveX.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings6, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761331"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a><span data-ttu-id="70df7-105">Interface IMsRdpClientAdvancedSettings6</span><span class="sxs-lookup"><span data-stu-id="70df7-105">IMsRdpClientAdvancedSettings6 interface</span></span>

<span data-ttu-id="70df7-106">Expõe as propriedades que gerenciam as configurações avançadas do controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="70df7-106">Exposes properties that manage advanced ActiveX control settings.</span></span> <span data-ttu-id="70df7-107">A interface **IMsRdpClientAdvancedSettings6** é derivada da interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="70df7-107">The **IMsRdpClientAdvancedSettings6** interface is derived from the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="70df7-108">Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="70df7-108">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="70df7-109">Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings6 de IID** para **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="70df7-109">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings6** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="70df7-110">Membros</span><span class="sxs-lookup"><span data-stu-id="70df7-110">Members</span></span>

<span data-ttu-id="70df7-111">A interface **IMsRdpClientAdvancedSettings6** herda de [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span><span class="sxs-lookup"><span data-stu-id="70df7-111">The **IMsRdpClientAdvancedSettings6** interface inherits from [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span></span> <span data-ttu-id="70df7-112">**IMsRdpClientAdvancedSettings6** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="70df7-112">**IMsRdpClientAdvancedSettings6** also has these types of members:</span></span>

-   [<span data-ttu-id="70df7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="70df7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70df7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="70df7-114">Properties</span></span>

<span data-ttu-id="70df7-115">A interface **IMsRdpClientAdvancedSettings6** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="70df7-115">The **IMsRdpClientAdvancedSettings6** interface has these properties.</span></span>



| <span data-ttu-id="70df7-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="70df7-116">Property</span></span>                                                                                                  | <span data-ttu-id="70df7-117">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="70df7-117">Access type</span></span>           | <span data-ttu-id="70df7-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="70df7-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70df7-119">**AuthenticationServiceClass**</span><span class="sxs-lookup"><span data-stu-id="70df7-119">**AuthenticationServiceClass**</span></span>](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | <span data-ttu-id="70df7-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70df7-120">Read/write</span></span><br/> | <span data-ttu-id="70df7-121">Especifica o nome da entidade de serviço (SPN) a ser usado para autenticação no servidor.</span><span class="sxs-lookup"><span data-stu-id="70df7-121">Specifies the service principal name (SPN) to use for authentication to the server.</span></span><br/>                                     |
| [<span data-ttu-id="70df7-122">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="70df7-122">**AuthenticationType**</span></span>](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | <span data-ttu-id="70df7-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="70df7-123">Read-only</span></span><br/>  | <span data-ttu-id="70df7-124">Especifica o tipo de autenticação usado para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="70df7-124">Specifies the type of authentication used for this connection.</span></span><br/>                                                          |
| [<span data-ttu-id="70df7-125">**ConnectToAdministerServer**</span><span class="sxs-lookup"><span data-stu-id="70df7-125">**ConnectToAdministerServer**</span></span>](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | <span data-ttu-id="70df7-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70df7-126">Read/write</span></span><br/> | <span data-ttu-id="70df7-127">Recupera ou especifica se o controle ActiveX deve tentar se conectar ao servidor para fins administrativos.</span><span class="sxs-lookup"><span data-stu-id="70df7-127">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span><br/> |
| [<span data-ttu-id="70df7-128">**EnableCredSspSupport**</span><span class="sxs-lookup"><span data-stu-id="70df7-128">**EnableCredSspSupport**</span></span>](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | <span data-ttu-id="70df7-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70df7-129">Read/write</span></span><br/> | <span data-ttu-id="70df7-130">Especifica se o provedor de serviços de segurança de credencial (CredSSP) está habilitado para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="70df7-130">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span><br/>                    |
| [<span data-ttu-id="70df7-131">**HotKeyFocusReleaseLeft**</span><span class="sxs-lookup"><span data-stu-id="70df7-131">**HotKeyFocusReleaseLeft**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | <span data-ttu-id="70df7-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70df7-132">Read/write</span></span><br/> | <span data-ttu-id="70df7-133">Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para CTRL + ALT + seta para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="70df7-133">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+LEFT ARROW.</span></span><br/>          |
| [<span data-ttu-id="70df7-134">**HotKeyFocusReleaseRight**</span><span class="sxs-lookup"><span data-stu-id="70df7-134">**HotKeyFocusReleaseRight**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | <span data-ttu-id="70df7-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70df7-135">Read/write</span></span><br/> | <span data-ttu-id="70df7-136">Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para CTRL + ALT + seta direita.</span><span class="sxs-lookup"><span data-stu-id="70df7-136">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+RIGHT ARROW.</span></span><br/>         |
| [<span data-ttu-id="70df7-137">**PCB**</span><span class="sxs-lookup"><span data-stu-id="70df7-137">**PCB**</span></span>](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | <span data-ttu-id="70df7-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70df7-138">Read/write</span></span><br/> | <span data-ttu-id="70df7-139">Especifica a configuração de BLOB de preconexão (PCB) a ser usada antes de se conectar para transmissão para o servidor.</span><span class="sxs-lookup"><span data-stu-id="70df7-139">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/>               |
| [<span data-ttu-id="70df7-140">**RelativeMouseMode**</span><span class="sxs-lookup"><span data-stu-id="70df7-140">**RelativeMouseMode**</span></span>](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | <span data-ttu-id="70df7-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70df7-141">Read/write</span></span><br/> | <span data-ttu-id="70df7-142">Especifica se o mouse deve usar o modo relativo.</span><span class="sxs-lookup"><span data-stu-id="70df7-142">Specifies whether the mouse should use relative mode.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="70df7-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="70df7-143">Remarks</span></span>

<span data-ttu-id="70df7-144">Essa interface foi estendida pela interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) , herdando todos os métodos e propriedades das interfaces anteriores.</span><span class="sxs-lookup"><span data-stu-id="70df7-144">This interface has been extended by the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface, inheriting all the methods and properties of the previous interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="70df7-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70df7-145">Requirements</span></span>



| <span data-ttu-id="70df7-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="70df7-146">Requirement</span></span> | <span data-ttu-id="70df7-147">Valor</span><span class="sxs-lookup"><span data-stu-id="70df7-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70df7-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70df7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="70df7-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70df7-149">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="70df7-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70df7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="70df7-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70df7-151">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="70df7-152">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="70df7-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="70df7-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70df7-153"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="70df7-154">DLL</span><span class="sxs-lookup"><span data-stu-id="70df7-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70df7-155"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70df7-155"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="70df7-156">IID</span><span class="sxs-lookup"><span data-stu-id="70df7-156">IID</span></span><br/>                      | <span data-ttu-id="70df7-157">IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="70df7-157">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70df7-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="70df7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70df7-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="70df7-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="70df7-160">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="70df7-160">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="70df7-161">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="70df7-161">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="70df7-162">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="70df7-162">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="70df7-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="70df7-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="70df7-164">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="70df7-164">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

