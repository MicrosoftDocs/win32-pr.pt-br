---
title: Propriedade IMsRdpClientAdvancedSettings6 AuthenticationType
description: Especifica o tipo de autenticação usado para essa conexão.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AuthenticationType
- Propriedade AuthenticationType Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade AuthenticationType
- Propriedade AuthenticationType Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade AuthenticationType
- Propriedade AuthenticationType Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade AuthenticationType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085559"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a><span data-ttu-id="126d4-110">Propriedade IMsRdpClientAdvancedSettings6:: AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="126d4-110">IMsRdpClientAdvancedSettings6::AuthenticationType property</span></span>

<span data-ttu-id="126d4-111">Especifica o tipo de autenticação usado para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="126d4-111">Specifies the type of authentication used for this connection.</span></span>

<span data-ttu-id="126d4-112">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="126d4-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="126d4-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="126d4-113">Syntax</span></span>


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a><span data-ttu-id="126d4-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="126d4-114">Property value</span></span>

<span data-ttu-id="126d4-115">Recebe um valor que especifica o tipo de autenticação usado para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="126d4-115">Receives a value that specifies the type of authentication used for this connection.</span></span> <span data-ttu-id="126d4-116">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="126d4-116">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="126d4-117">0</span><span class="sxs-lookup"><span data-stu-id="126d4-117">0</span></span>
</dt> <dd>

<span data-ttu-id="126d4-118">Nenhuma autenticação é usada.</span><span class="sxs-lookup"><span data-stu-id="126d4-118">No authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="126d4-119">1</span><span class="sxs-lookup"><span data-stu-id="126d4-119">1</span></span>
</dt> <dd>

<span data-ttu-id="126d4-120">A autenticação de certificado é usada.</span><span class="sxs-lookup"><span data-stu-id="126d4-120">Certificate authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="126d4-121">2</span><span class="sxs-lookup"><span data-stu-id="126d4-121">2</span></span>
</dt> <dd>

<span data-ttu-id="126d4-122">A autenticação Kerberos é usada.</span><span class="sxs-lookup"><span data-stu-id="126d4-122">Kerberos authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="126d4-123">3</span><span class="sxs-lookup"><span data-stu-id="126d4-123">3</span></span>
</dt> <dd>

<span data-ttu-id="126d4-124">O certificado e a autenticação Kerberos são usados.</span><span class="sxs-lookup"><span data-stu-id="126d4-124">Both certificate and Kerberos authentication are used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="126d4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="126d4-125">Requirements</span></span>



| <span data-ttu-id="126d4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="126d4-126">Requirement</span></span> | <span data-ttu-id="126d4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="126d4-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="126d4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="126d4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="126d4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="126d4-129">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="126d4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="126d4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="126d4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="126d4-131">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="126d4-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="126d4-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="126d4-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="126d4-133"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="126d4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="126d4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="126d4-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="126d4-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="126d4-136">IID</span><span class="sxs-lookup"><span data-stu-id="126d4-136">IID</span></span><br/>                      | <span data-ttu-id="126d4-137">IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="126d4-137">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="126d4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="126d4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="126d4-139">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="126d4-139">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="126d4-140">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="126d4-140">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="126d4-141">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="126d4-141">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





