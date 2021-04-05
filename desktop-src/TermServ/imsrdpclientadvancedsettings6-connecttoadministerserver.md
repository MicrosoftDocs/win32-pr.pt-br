---
title: Propriedade IMsRdpClientAdvancedSettings6 ConnectToAdministerServer
description: Recupera ou especifica se o controle ActiveX deve tentar se conectar ao servidor para fins administrativos.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectToAdministerServer
- Propriedade ConnectToAdministerServer Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade ConnectToAdministerServer
- Propriedade ConnectToAdministerServer Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade ConnectToAdministerServer
- Propriedade ConnectToAdministerServer Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ConnectToAdministerServer
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009374"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a><span data-ttu-id="e0917-110">Propriedade IMsRdpClientAdvancedSettings6:: ConnectToAdministerServer</span><span class="sxs-lookup"><span data-stu-id="e0917-110">IMsRdpClientAdvancedSettings6::ConnectToAdministerServer property</span></span>

<span data-ttu-id="e0917-111">Recupera ou especifica se o controle ActiveX deve tentar se conectar ao servidor para fins administrativos.</span><span class="sxs-lookup"><span data-stu-id="e0917-111">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span>

<span data-ttu-id="e0917-112">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e0917-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0917-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0917-113">Syntax</span></span>


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a><span data-ttu-id="e0917-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e0917-114">Property value</span></span>

<span data-ttu-id="e0917-115">**Variante \_ TRUE** para fazer com que o controle ActiveX tente se conectar ao servidor para fins administrativos; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e0917-115">**VARIANT\_TRUE** to cause the ActiveX control to attempt to connect to the server for administrative purposes; otherwise **VARIANT\_FALSE**.</span></span> <span data-ttu-id="e0917-116">O valor padrão é **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e0917-116">The default value is **VARIANT\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0917-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0917-117">Remarks</span></span>

<span data-ttu-id="e0917-118">Para usar o **ConnectToAdministerServer**, você deve estar executando conexão de área de trabalho remota (RDC) cliente versão 6,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e0917-118">To use **ConnectToAdministerServer**, you must be running Remote Desktop Connection (RDC) client version 6.1 or later.</span></span>

> [!Note]  
> <span data-ttu-id="e0917-119">A RDC versão 6,1 (6.0.6001) dá suporte a protocolo RDP 6,1.</span><span class="sxs-lookup"><span data-stu-id="e0917-119">RDC version 6.1 (6.0.6001) supports Remote Desktop Protocol 6.1.</span></span> <span data-ttu-id="e0917-120">O RDC 6,1 está incluído no Windows Server 2008 e no Windows Vista com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e0917-120">RDC 6.1 is included with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

 

<span data-ttu-id="e0917-121">**ConnectToAdministerServer** conecta você a uma sessão que é usada para fins administrativos no servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="e0917-121">**ConnectToAdministerServer** connects you to a session that is used for administrative purposes on the remote server.</span></span> <span data-ttu-id="e0917-122">Se o serviço de função Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) estiver instalado no servidor remoto, o **ConnectToAdministerServer** fará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e0917-122">If the Remote Desktop Session Host (RD Session Host) role service is installed on the remote server, **ConnectToAdministerServer** does the following:</span></span>

-   <span data-ttu-id="e0917-123">Desabilita Serviços de Área de Trabalho Remota licenciamento de acesso para cliente para a sessão.</span><span class="sxs-lookup"><span data-stu-id="e0917-123">Disables Remote Desktop Services client access licensing for the session.</span></span>
-   <span data-ttu-id="e0917-124">Desabilita o redirecionamento de fuso horário para a sessão.</span><span class="sxs-lookup"><span data-stu-id="e0917-124">Disables time zone redirection for the session.</span></span>
-   <span data-ttu-id="e0917-125">Desabilita o redirecionamento de Conexão de Área de Trabalho Remota Agente de conexão de área de trabalho remota para a sessão.</span><span class="sxs-lookup"><span data-stu-id="e0917-125">Disables Remote Desktop Connection Broker (RD Connection Broker) redirection for the session.</span></span>
-   <span data-ttu-id="e0917-126">Desabilita o redirecionamento de dispositivo Plug and Play para a sessão.</span><span class="sxs-lookup"><span data-stu-id="e0917-126">Disables Plug and Play device redirection for the session.</span></span>
-   <span data-ttu-id="e0917-127">Altera o tema da sessão remota para o Windows clássico para a sessão.</span><span class="sxs-lookup"><span data-stu-id="e0917-127">Changes the remote session theme to Windows Classic for the session.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0917-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0917-128">Requirements</span></span>



| <span data-ttu-id="e0917-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0917-129">Requirement</span></span> | <span data-ttu-id="e0917-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e0917-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0917-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0917-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e0917-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0917-132">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="e0917-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0917-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e0917-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0917-134">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e0917-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e0917-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0917-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0917-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e0917-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e0917-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0917-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0917-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e0917-139">IID</span><span class="sxs-lookup"><span data-stu-id="e0917-139">IID</span></span><br/>                      | <span data-ttu-id="e0917-140">IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="e0917-140">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0917-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0917-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0917-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e0917-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e0917-143">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e0917-143">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e0917-144">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e0917-144">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





