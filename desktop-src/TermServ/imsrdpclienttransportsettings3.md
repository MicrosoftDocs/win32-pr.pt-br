---
title: Interface IMsRdpClientTransportSettings3
description: Define propriedades adicionais para o servidor de gateway de Área de Trabalho Remota (Gateway RD). | Interface IMsRdpClientTransportSettings3
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings3
- Serviços de Área de Trabalho Remota da interface IMsRdpClientTransportSettings3, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837757"
---
# <a name="imsrdpclienttransportsettings3-interface"></a><span data-ttu-id="1a1e3-106">Interface IMsRdpClientTransportSettings3</span><span class="sxs-lookup"><span data-stu-id="1a1e3-106">IMsRdpClientTransportSettings3 interface</span></span>

<span data-ttu-id="1a1e3-107">Define propriedades adicionais para o servidor de gateway de Área de Trabalho Remota (Gateway RD).</span><span class="sxs-lookup"><span data-stu-id="1a1e3-107">Defines additional properties for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="1a1e3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1a1e3-108">Members</span></span>

<span data-ttu-id="1a1e3-109">A interface **IMsRdpClientTransportSettings3** herda de [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="1a1e3-109">The **IMsRdpClientTransportSettings3** interface inherits from [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span></span> <span data-ttu-id="1a1e3-110">**IMsRdpClientTransportSettings3** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1a1e3-110">**IMsRdpClientTransportSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="1a1e3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a1e3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a1e3-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a1e3-112">Properties</span></span>

<span data-ttu-id="1a1e3-113">A interface **IMsRdpClientTransportSettings3** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1a1e3-113">The **IMsRdpClientTransportSettings3** interface has these properties.</span></span>



| <span data-ttu-id="1a1e3-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1a1e3-114">Property</span></span>                                                                                                           | <span data-ttu-id="1a1e3-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="1a1e3-115">Access type</span></span>           | <span data-ttu-id="1a1e3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a1e3-116">Description</span></span>                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a1e3-117">**GatewayAuthCookieServerAddr**</span><span class="sxs-lookup"><span data-stu-id="1a1e3-117">**GatewayAuthCookieServerAddr**</span></span>](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | <span data-ttu-id="1a1e3-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1a1e3-118">Read/write</span></span><br/> | <span data-ttu-id="1a1e3-119">O endereço do servidor para autenticação baseada em cookie.</span><span class="sxs-lookup"><span data-stu-id="1a1e3-119">The server address for cookie-based authentication.</span></span><br/>                                                                                       |
| [<span data-ttu-id="1a1e3-120">**GatewayAuthLoginPage**</span><span class="sxs-lookup"><span data-stu-id="1a1e3-120">**GatewayAuthLoginPage**</span></span>](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | <span data-ttu-id="1a1e3-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1a1e3-121">Read/write</span></span><br/> | <span data-ttu-id="1a1e3-122">O endereço da página da Web de logon a ser usada para autenticar um usuário.</span><span class="sxs-lookup"><span data-stu-id="1a1e3-122">The address of the login webpage to use to authenticate a user.</span></span><br/>                                                                           |
| [<span data-ttu-id="1a1e3-123">**GatewayCredSourceCookie**</span><span class="sxs-lookup"><span data-stu-id="1a1e3-123">**GatewayCredSourceCookie**</span></span>](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | <span data-ttu-id="1a1e3-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1a1e3-124">Read/write</span></span><br/> | <span data-ttu-id="1a1e3-125">Especifica se a origem da credencial é baseada em cookie.</span><span class="sxs-lookup"><span data-stu-id="1a1e3-125">Specifies if the credential source is cookie based.</span></span><br/>                                                                                       |
| [<span data-ttu-id="1a1e3-126">**GatewayEncryptedAuthCookie**</span><span class="sxs-lookup"><span data-stu-id="1a1e3-126">**GatewayEncryptedAuthCookie**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | <span data-ttu-id="1a1e3-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1a1e3-127">Read/write</span></span><br/> | <span data-ttu-id="1a1e3-128">O cookie de autenticação criptografado.</span><span class="sxs-lookup"><span data-stu-id="1a1e3-128">The encrypted authentication cookie.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="1a1e3-129">**GatewayEncryptedAuthCookieSize**</span><span class="sxs-lookup"><span data-stu-id="1a1e3-129">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | <span data-ttu-id="1a1e3-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1a1e3-130">Read/write</span></span><br/> | <span data-ttu-id="1a1e3-131">O tamanho, em caracteres, da propriedade [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .</span><span class="sxs-lookup"><span data-stu-id="1a1e3-131">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1a1e3-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a1e3-132">Requirements</span></span>



| <span data-ttu-id="1a1e3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a1e3-133">Requirement</span></span> | <span data-ttu-id="1a1e3-134">Valor</span><span class="sxs-lookup"><span data-stu-id="1a1e3-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a1e3-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a1e3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1a1e3-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1a1e3-136">Windows 7</span></span><br/>                                                                              |
| <span data-ttu-id="1a1e3-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a1e3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1a1e3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a1e3-138">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="1a1e3-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1a1e3-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="1a1e3-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e3-140"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="1a1e3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1a1e3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a1e3-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a1e3-142"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="1a1e3-143">IID</span><span class="sxs-lookup"><span data-stu-id="1a1e3-143">IID</span></span><br/>                      | <span data-ttu-id="1a1e3-144">IID \_ IMsRdpClientTransportSettings3 é definido como 3D5B21AC-748D-41DE-8F30-E15169586BD4</span><span class="sxs-lookup"><span data-stu-id="1a1e3-144">IID\_IMsRdpClientTransportSettings3 is defined as 3D5B21AC-748D-41DE-8F30-E15169586BD4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a1e3-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a1e3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a1e3-146">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="1a1e3-146">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





