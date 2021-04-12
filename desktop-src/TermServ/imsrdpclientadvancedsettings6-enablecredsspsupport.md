---
title: Propriedade IMsRdpClientAdvancedSettings6 EnableCredSspSupport
description: Especifica se o provedor de serviços de segurança de credencial (CredSSP) está habilitado para esta conexão.
ms.assetid: 3BC8A265-7AEA-4C9C-9730-7710E1A3159D
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade EnableCredSspSupport
- Propriedade EnableCredSspSupport Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.put_EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73ad2b024cd0f8bbcafd6ba05be093c5953d54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499367"
---
# <a name="imsrdpclientadvancedsettings6enablecredsspsupport-property"></a><span data-ttu-id="65f18-110">Propriedade IMsRdpClientAdvancedSettings6:: EnableCredSspSupport</span><span class="sxs-lookup"><span data-stu-id="65f18-110">IMsRdpClientAdvancedSettings6::EnableCredSspSupport property</span></span>

<span data-ttu-id="65f18-111">Especifica se o provedor de serviços de segurança de credencial (CredSSP) está habilitado para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="65f18-111">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="65f18-112">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="65f18-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f18-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="65f18-113">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="65f18-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="65f18-114">Property value</span></span>

<span data-ttu-id="65f18-115">Especifica se o CredSSP está habilitado para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="65f18-115">Specifies whether CredSSP is enabled for this connection.</span></span> <span data-ttu-id="65f18-116">Defina como **Variant \_ true** para habilitar CredSSP ou **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="65f18-116">Set to **VARIANT\_TRUE** to enable CredSSP or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="65f18-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="65f18-117">Remarks</span></span>

<span data-ttu-id="65f18-118">Essa propriedade só tem suporte nos clientes Conexão de Área de Trabalho Remota 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="65f18-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="65f18-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65f18-119">Requirements</span></span>



| <span data-ttu-id="65f18-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f18-120">Requirement</span></span> | <span data-ttu-id="65f18-121">Valor</span><span class="sxs-lookup"><span data-stu-id="65f18-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f18-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65f18-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65f18-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65f18-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="65f18-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65f18-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65f18-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65f18-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="65f18-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="65f18-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="65f18-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65f18-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="65f18-128">DLL</span><span class="sxs-lookup"><span data-stu-id="65f18-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65f18-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65f18-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="65f18-130">IID</span><span class="sxs-lookup"><span data-stu-id="65f18-130">IID</span></span><br/>                      | <span data-ttu-id="65f18-131">IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="65f18-131">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65f18-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="65f18-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f18-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="65f18-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="65f18-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="65f18-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="65f18-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="65f18-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





