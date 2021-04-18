---
title: Método SetPromptForPassword da classe Win32_TSLogonSetting
description: O método SetPromptForPassword define a propriedade PromptForPassword.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetPromptForPassword
- Método SetPromptForPassword Serviços de Área de Trabalho Remota, classe Win32_TSLogonSetting
- Classe Win32_TSLogonSetting Serviços de Área de Trabalho Remota, método SetPromptForPassword
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756798"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="a3f72-106">Método SetPromptForPassword da classe Win32 \_ TSLogonSetting</span><span class="sxs-lookup"><span data-stu-id="a3f72-106">SetPromptForPassword method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="a3f72-107">O método **SetPromptForPassword** define a propriedade **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="a3f72-107">The **SetPromptForPassword** method sets the **PromptForPassword** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f72-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3f72-108">Syntax</span></span>


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a><span data-ttu-id="a3f72-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3f72-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f72-110">*PromptForPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a3f72-110">*PromptForPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f72-111">Sinalizador desabilitando ou habilitando a propriedade **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="a3f72-111">Flag disabling or enabling the **PromptForPassword** property.</span></span>

<dt>

<span data-ttu-id="a3f72-112">0</span><span class="sxs-lookup"><span data-stu-id="a3f72-112">0</span></span>
</dt> <dd>

<span data-ttu-id="a3f72-113">Desabilita a solicitação de senha.</span><span class="sxs-lookup"><span data-stu-id="a3f72-113">Disables password-prompting.</span></span>

</dd> <dt>

<span data-ttu-id="a3f72-114">1</span><span class="sxs-lookup"><span data-stu-id="a3f72-114">1</span></span>
</dt> <dd>

<span data-ttu-id="a3f72-115">Habilita a solicitação de senha.</span><span class="sxs-lookup"><span data-stu-id="a3f72-115">Enables password-prompting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f72-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3f72-116">Return value</span></span>

<span data-ttu-id="a3f72-117">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="a3f72-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a3f72-118">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="a3f72-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a3f72-119">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a3f72-119">The method returns an error if the setting is under group policy control.</span></span>

<dl> <dt>

<span data-ttu-id="a3f72-120">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="a3f72-120">**FALSE** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a3f72-121">**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="a3f72-121">**TRUE** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a3f72-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3f72-122">Remarks</span></span>

<span data-ttu-id="a3f72-123">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a3f72-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a3f72-124">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a3f72-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a3f72-125">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a3f72-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a3f72-126">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a3f72-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f72-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3f72-127">Requirements</span></span>



| <span data-ttu-id="a3f72-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f72-128">Requirement</span></span> | <span data-ttu-id="a3f72-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a3f72-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f72-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3f72-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f72-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3f72-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3f72-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3f72-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f72-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3f72-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3f72-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3f72-134">Namespace</span></span><br/>                | <span data-ttu-id="a3f72-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a3f72-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a3f72-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a3f72-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3f72-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3f72-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3f72-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a3f72-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3f72-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3f72-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f72-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3f72-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f72-141">**\_TSLogonSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a3f72-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

