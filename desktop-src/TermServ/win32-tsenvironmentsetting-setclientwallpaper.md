---
title: Método SetClientWallPaper da classe Win32_TSEnvironmentSetting
description: O método SetClientWallPaper define a propriedade ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetClientWallPaper
- Método SetClientWallPaper Serviços de Área de Trabalho Remota, classe Win32_TSEnvironmentSetting
- Classe Win32_TSEnvironmentSetting Serviços de Área de Trabalho Remota, método SetClientWallPaper
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644589"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="69df9-106">Método SetClientWallPaper da classe Win32 \_ TSEnvironmentSetting</span><span class="sxs-lookup"><span data-stu-id="69df9-106">SetClientWallPaper method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="69df9-107">O método **SetClientWallPaper** define a propriedade **ClientWallPaper** .</span><span class="sxs-lookup"><span data-stu-id="69df9-107">The **SetClientWallPaper** method sets the **ClientWallPaper** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="69df9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69df9-108">Syntax</span></span>


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a><span data-ttu-id="69df9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69df9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69df9-110">*ClientWallPaper* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69df9-110">*ClientWallPaper* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69df9-111">Sinalizador desabilitando ou habilitando a propriedade **ClientWallPaper** , que especifica se a imagem de plano de fundo (ou papel de parede) é exibida no cliente.</span><span class="sxs-lookup"><span data-stu-id="69df9-111">Flag disabling or enabling the **ClientWallPaper** property, which specifies whether the background (or wallpaper) image is displayed on the client.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="69df9-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="69df9-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="69df9-113">A imagem em segundo plano (ou papel de parede) não é exibida no cliente.</span><span class="sxs-lookup"><span data-stu-id="69df9-113">The background (or wallpaper) image is not displayed on the client.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="69df9-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="69df9-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="69df9-115">A imagem em segundo plano (ou papel de parede) é exibida no cliente.</span><span class="sxs-lookup"><span data-stu-id="69df9-115">The background (or wallpaper) image is displayed on the client.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69df9-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69df9-116">Return value</span></span>

<span data-ttu-id="69df9-117">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="69df9-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="69df9-118">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="69df9-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="69df9-119">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="69df9-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="69df9-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="69df9-120">Remarks</span></span>

<span data-ttu-id="69df9-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="69df9-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="69df9-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="69df9-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="69df9-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="69df9-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="69df9-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="69df9-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="69df9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69df9-125">Requirements</span></span>



| <span data-ttu-id="69df9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="69df9-126">Requirement</span></span> | <span data-ttu-id="69df9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="69df9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69df9-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69df9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="69df9-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69df9-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69df9-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69df9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="69df9-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69df9-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69df9-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="69df9-132">Namespace</span></span><br/>                | <span data-ttu-id="69df9-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="69df9-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="69df9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="69df9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69df9-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69df9-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="69df9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="69df9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69df9-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69df9-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69df9-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="69df9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69df9-139">**\_TSEnvironmentSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="69df9-139">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

