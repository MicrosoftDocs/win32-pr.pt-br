---
title: Propriedade IMsTscSecuredSettings WorkDir
description: Especifica o diretório de trabalho do programa de início.
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade WorkDir
- Propriedade WorkDir Serviços de Área de Trabalho Remota, interface IMsTscSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsTscSecuredSettings, Propriedade WorkDir
- Propriedade WorkDir Serviços de Área de Trabalho Remota, interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings, Propriedade WorkDir
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0a80b35ba682012150b4277d800bc4a3582e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757594"
---
# <a name="imstscsecuredsettingsworkdir-property"></a><span data-ttu-id="5128b-108">Propriedade IMsTscSecuredSettings:: WorkDir</span><span class="sxs-lookup"><span data-stu-id="5128b-108">IMsTscSecuredSettings::WorkDir property</span></span>

<span data-ttu-id="5128b-109">Especifica o diretório de trabalho do programa de início.</span><span class="sxs-lookup"><span data-stu-id="5128b-109">Specifies the working directory of the start program.</span></span>

<span data-ttu-id="5128b-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5128b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5128b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5128b-111">Syntax</span></span>


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a><span data-ttu-id="5128b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5128b-112">Property value</span></span>

<span data-ttu-id="5128b-113">O novo diretório de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5128b-113">The new working directory.</span></span> <span data-ttu-id="5128b-114">O comprimento máximo dessa cadeia de caracteres é o **\_ caminho máximo**-1 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5128b-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5128b-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5128b-115">Error codes</span></span>

<span data-ttu-id="5128b-116">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5128b-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5128b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5128b-117">Remarks</span></span>

<span data-ttu-id="5128b-118">Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5128b-118">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="5128b-119">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5128b-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5128b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5128b-120">Requirements</span></span>



| <span data-ttu-id="5128b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5128b-121">Requirement</span></span> | <span data-ttu-id="5128b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5128b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5128b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5128b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5128b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5128b-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5128b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5128b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5128b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5128b-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5128b-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5128b-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="5128b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5128b-128"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="5128b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5128b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5128b-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5128b-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="5128b-131">IID</span><span class="sxs-lookup"><span data-stu-id="5128b-131">IID</span></span><br/>                      | <span data-ttu-id="5128b-132">IID \_ IMsTscSecuredSettings é definido como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="5128b-132">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5128b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5128b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5128b-134">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="5128b-134">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5128b-135">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="5128b-135">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





