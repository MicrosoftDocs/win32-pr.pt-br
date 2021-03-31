---
title: Método SetSessionDirectoryActive da classe Win32_TSSessionDirectory
description: O método SetSessionDirectoryActive define a propriedade SessionDirectoryActive.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSessionDirectoryActive
- Método SetSessionDirectoryActive Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetSessionDirectoryActive
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca8709028ee90db549c7cdeb053b04dc88b52ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369507"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="2c8b5-106">Método SetSessionDirectoryActive da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="2c8b5-106">SetSessionDirectoryActive method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="2c8b5-107">O método **SetSessionDirectoryActive** define a propriedade **SessionDirectoryActive** .</span><span class="sxs-lookup"><span data-stu-id="2c8b5-107">The **SetSessionDirectoryActive** method sets the **SessionDirectoryActive** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8b5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c8b5-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a><span data-ttu-id="2c8b5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c8b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8b5-110">*SessionDirectoryActive* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c8b5-110">*SessionDirectoryActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8b5-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c8b5-111">Type: **uint32**</span></span>

<span data-ttu-id="2c8b5-112">Sinalizador desabilitando ou habilitando o serviço de diretório de sessões.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-112">Flag disabling or enabling the Session Directory service.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="2c8b5-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="2c8b5-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="2c8b5-114">Desabilite o serviço de diretório de sessões.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-114">Disable the Session Directory service.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="2c8b5-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="2c8b5-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="2c8b5-116">Habilite o serviço de diretório de sessões.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-116">Enable the Session Directory service.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8b5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c8b5-117">Return value</span></span>

<span data-ttu-id="2c8b5-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c8b5-118">Type: **uint32**</span></span>

<span data-ttu-id="2c8b5-119">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2c8b5-120">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="2c8b5-121">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c8b5-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c8b5-122">Remarks</span></span>

<span data-ttu-id="2c8b5-123">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2c8b5-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2c8b5-124">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2c8b5-125">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2c8b5-126">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2c8b5-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8b5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c8b5-127">Requirements</span></span>



| <span data-ttu-id="2c8b5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c8b5-128">Requirement</span></span> | <span data-ttu-id="2c8b5-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2c8b5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8b5-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c8b5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8b5-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2c8b5-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2c8b5-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c8b5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8b5-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c8b5-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c8b5-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c8b5-134">Namespace</span></span><br/>                | <span data-ttu-id="2c8b5-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="2c8b5-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2c8b5-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2c8b5-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c8b5-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c8b5-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c8b5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2c8b5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c8b5-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c8b5-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8b5-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2c8b5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8b5-141">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="2c8b5-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

