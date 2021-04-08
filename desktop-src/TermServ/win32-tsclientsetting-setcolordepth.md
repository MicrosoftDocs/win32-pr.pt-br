---
title: Método SetColorDepth da classe Win32_TSClientSetting
description: O método SetColorDepth define a propriedade ColorDepth para a classe.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetColorDepth
- Método SetColorDepth Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método SetColorDepth
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919036"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="12484-106">Método SetColorDepth da classe Win32 \_ TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="12484-106">SetColorDepth method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="12484-107">O método **SetColorDepth** define a propriedade **ColorDepth** para a classe.</span><span class="sxs-lookup"><span data-stu-id="12484-107">The **SetColorDepth** method sets the **ColorDepth** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="12484-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12484-108">Syntax</span></span>


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a><span data-ttu-id="12484-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12484-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12484-110">*ColorDepth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12484-110">*ColorDepth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12484-111">O novo valor para a propriedade **ColorDepth** .</span><span class="sxs-lookup"><span data-stu-id="12484-111">The new value for the **ColorDepth** property.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="12484-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="12484-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="12484-113">8 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="12484-113">8 bits per pixel</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="12484-114"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="12484-114"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="12484-115">15 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="12484-115">15 bits per pixel</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="12484-116"><span id="3"></span>**Beta**</span><span class="sxs-lookup"><span data-stu-id="12484-116"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="12484-117">16 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="12484-117">16 bits per pixel</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="12484-118"><span id="4"></span>**quatro**</span><span class="sxs-lookup"><span data-stu-id="12484-118"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="12484-119">24 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="12484-119">24 bits per pixel</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="12484-120"><span id="5"></span>**05**</span><span class="sxs-lookup"><span data-stu-id="12484-120"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="12484-121">32 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="12484-121">32 bits per pixel</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12484-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12484-122">Return value</span></span>

<span data-ttu-id="12484-123">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="12484-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="12484-124">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="12484-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="12484-125">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="12484-125">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="12484-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="12484-126">Remarks</span></span>

<span data-ttu-id="12484-127">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="12484-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="12484-128">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="12484-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="12484-129">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="12484-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="12484-130">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="12484-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="12484-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12484-131">Requirements</span></span>



| <span data-ttu-id="12484-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="12484-132">Requirement</span></span> | <span data-ttu-id="12484-133">Valor</span><span class="sxs-lookup"><span data-stu-id="12484-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12484-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12484-134">Minimum supported client</span></span><br/> | <span data-ttu-id="12484-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12484-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12484-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12484-136">Minimum supported server</span></span><br/> | <span data-ttu-id="12484-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12484-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12484-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="12484-138">Namespace</span></span><br/>                | <span data-ttu-id="12484-139">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="12484-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="12484-140">MOF</span><span class="sxs-lookup"><span data-stu-id="12484-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12484-141"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12484-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="12484-142">DLL</span><span class="sxs-lookup"><span data-stu-id="12484-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12484-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12484-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12484-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="12484-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12484-145">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="12484-145">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

