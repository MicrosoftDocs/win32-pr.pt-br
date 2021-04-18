---
title: Método InitialProgram da classe Win32_TSEnvironmentSetting
description: O método InitialProgram define as propriedades do programa de inicialização, como o nome, o diretório de trabalho e o caminho do programa para iniciar imediatamente após o logon no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InitialProgram
- Método InitialProgram Serviços de Área de Trabalho Remota, classe Win32_TSEnvironmentSetting
- Classe Win32_TSEnvironmentSetting Serviços de Área de Trabalho Remota, método InitialProgram
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760120"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="ed8ba-106">Método InitialProgram da classe Win32 \_ TSEnvironmentSetting</span><span class="sxs-lookup"><span data-stu-id="ed8ba-106">InitialProgram method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="ed8ba-107">O método **InitialProgram** define as propriedades do programa de inicialização, como o nome, o diretório de trabalho e o caminho do programa para iniciar imediatamente após o logon no servidor de Host da Sessão da Área de Trabalho Remota (host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="ed8ba-107">The **InitialProgram** method sets startup program properties such as the name, working directory, and path of the program to start immediately after logon to the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8ba-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed8ba-108">Syntax</span></span>


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a><span data-ttu-id="ed8ba-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed8ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8ba-110">*InitialProgramPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed8ba-110">*InitialProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8ba-111">O nome e o caminho do programa de inicialização.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-111">The name and path of the startup program.</span></span>

</dd> <dt>

<span data-ttu-id="ed8ba-112">*Início* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed8ba-112">*Startin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8ba-113">O caminho para o diretório de trabalho do programa de inicialização.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-113">The path to the working directory of the startup program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed8ba-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed8ba-114">Return value</span></span>

<span data-ttu-id="ed8ba-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ed8ba-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="ed8ba-117">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed8ba-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed8ba-118">Remarks</span></span>

<span data-ttu-id="ed8ba-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ed8ba-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ed8ba-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ed8ba-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ed8ba-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ed8ba-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8ba-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed8ba-123">Requirements</span></span>



| <span data-ttu-id="ed8ba-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed8ba-124">Requirement</span></span> | <span data-ttu-id="ed8ba-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ed8ba-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8ba-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed8ba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8ba-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed8ba-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed8ba-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed8ba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8ba-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed8ba-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed8ba-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed8ba-130">Namespace</span></span><br/>                | <span data-ttu-id="ed8ba-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="ed8ba-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ed8ba-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ed8ba-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed8ba-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed8ba-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed8ba-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ed8ba-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed8ba-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed8ba-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed8ba-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed8ba-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8ba-137">**\_TSEnvironmentSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="ed8ba-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

