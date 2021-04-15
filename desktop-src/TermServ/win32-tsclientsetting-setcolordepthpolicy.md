---
title: Método SetColorDepthPolicy da classe Win32_TSClientSetting
description: O método SetColorDepthPolicy define a propriedade ColorDepthPolicy para a classe.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetColorDepthPolicy
- Método SetColorDepthPolicy Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método SetColorDepthPolicy
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d47280ce303e7eeba401e0eb34c7f7fa5a7bec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369555"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="2b556-106">Método SetColorDepthPolicy da classe Win32 \_ TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="2b556-106">SetColorDepthPolicy method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="2b556-107">O método **SetColorDepthPolicy** define a propriedade **ColorDepthPolicy** para a classe.</span><span class="sxs-lookup"><span data-stu-id="2b556-107">The **SetColorDepthPolicy** method sets the **ColorDepthPolicy** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b556-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b556-108">Syntax</span></span>


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="2b556-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b556-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b556-110">*ColorDepthPolicy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b556-110">*ColorDepthPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b556-111">Sinalizador desabilitando ou habilitando a propriedade **SetColorDepthPolicy** , que especifica se a configuração de cor máxima do usuário deve ser substituída.</span><span class="sxs-lookup"><span data-stu-id="2b556-111">Flag disabling or enabling the **SetColorDepthPolicy** property, which specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="2b556-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="2b556-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="2b556-113">Habilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="2b556-113">Enable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="2b556-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="2b556-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="2b556-115">Desabilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="2b556-115">Disable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b556-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b556-116">Return value</span></span>

<span data-ttu-id="2b556-117">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="2b556-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2b556-118">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="2b556-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="2b556-119">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="2b556-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b556-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b556-120">Remarks</span></span>

<span data-ttu-id="2b556-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2b556-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2b556-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2b556-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2b556-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="2b556-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2b556-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2b556-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b556-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b556-125">Requirements</span></span>



| <span data-ttu-id="2b556-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b556-126">Requirement</span></span> | <span data-ttu-id="2b556-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2b556-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b556-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b556-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2b556-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b556-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b556-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b556-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2b556-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b556-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b556-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b556-132">Namespace</span></span><br/>                | <span data-ttu-id="2b556-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="2b556-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2b556-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2b556-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b556-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b556-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b556-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2b556-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b556-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b556-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b556-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b556-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b556-139">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="2b556-139">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

