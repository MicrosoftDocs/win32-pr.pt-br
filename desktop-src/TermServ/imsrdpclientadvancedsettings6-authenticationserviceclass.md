---
title: Propriedade IMsRdpClientAdvancedSettings6 AuthenticationServiceClass
description: Especifica o nome da entidade de serviço (SPN) a ser usado para autenticação no servidor.
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AuthenticationServiceClass
- Propriedade AuthenticationServiceClass Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade AuthenticationServiceClass
- Propriedade AuthenticationServiceClass Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade AuthenticationServiceClass
- Propriedade AuthenticationServiceClass Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade AuthenticationServiceClass
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.put_AuthenticationServiceClass
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618b55d1489f46e0e1119186bd5003fb68dbfebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644654"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a><span data-ttu-id="84740-110">Propriedade IMsRdpClientAdvancedSettings6:: AuthenticationServiceClass</span><span class="sxs-lookup"><span data-stu-id="84740-110">IMsRdpClientAdvancedSettings6::AuthenticationServiceClass property</span></span>

<span data-ttu-id="84740-111">Especifica o nome da entidade de serviço (SPN) a ser usado para autenticação no servidor.</span><span class="sxs-lookup"><span data-stu-id="84740-111">Specifies the service principal name (SPN) to use for authentication to the server.</span></span>

<span data-ttu-id="84740-112">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="84740-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="84740-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84740-113">Syntax</span></span>


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a><span data-ttu-id="84740-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="84740-114">Property value</span></span>

<span data-ttu-id="84740-115">Especifica o nome da entidade de serviço a ser usada.</span><span class="sxs-lookup"><span data-stu-id="84740-115">Specifies the service principal name to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="84740-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="84740-116">Remarks</span></span>

<span data-ttu-id="84740-117">Essa propriedade só tem suporte nos clientes Conexão de Área de Trabalho Remota 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="84740-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="84740-118">Os SPNs (nomes da entidade de serviço) são associados à entidade de segurança (usuário ou grupos) em cujo contexto de segurança o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="84740-118">Service principal names (SPNs) are associated with the security principal (user or groups) in whose security context the service executes.</span></span> <span data-ttu-id="84740-119">Os SPNs são usados para dar suporte à autenticação mútua entre um aplicativo cliente e um serviço.</span><span class="sxs-lookup"><span data-stu-id="84740-119">SPNs are used to support mutual authentication between a client application and a service.</span></span>

## <a name="requirements"></a><span data-ttu-id="84740-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84740-120">Requirements</span></span>



| <span data-ttu-id="84740-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="84740-121">Requirement</span></span> | <span data-ttu-id="84740-122">Valor</span><span class="sxs-lookup"><span data-stu-id="84740-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84740-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84740-123">Minimum supported client</span></span><br/> | <span data-ttu-id="84740-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84740-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="84740-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84740-125">Minimum supported server</span></span><br/> | <span data-ttu-id="84740-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84740-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="84740-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="84740-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="84740-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84740-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="84740-129">DLL</span><span class="sxs-lookup"><span data-stu-id="84740-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84740-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84740-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="84740-131">IID</span><span class="sxs-lookup"><span data-stu-id="84740-131">IID</span></span><br/>                      | <span data-ttu-id="84740-132">IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="84740-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84740-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="84740-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84740-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="84740-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="84740-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="84740-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="84740-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="84740-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





