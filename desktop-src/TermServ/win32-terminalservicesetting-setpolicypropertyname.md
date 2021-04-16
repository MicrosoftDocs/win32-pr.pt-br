---
title: Método SetPolicyPropertyName da classe Win32_TerminalServiceSetting
description: O método SetPolicyPropertyName define a propriedade DeleteTempFolders, UseTempFolders ou help para a classe.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetPolicyPropertyName
- Método SetPolicyPropertyName Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetPolicyPropertyName
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455851"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f6c4d-106">Método SetPolicyPropertyName da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="f6c4d-106">SetPolicyPropertyName method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f6c4d-107">O método **SetPolicyPropertyName** define a propriedade **DeleteTempFolders**, **UseTempFolders** ou **Help** para a classe.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-107">The **SetPolicyPropertyName** method sets the **DeleteTempFolders**, **UseTempFolders** or **Help** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c4d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6c4d-108">Syntax</span></span>


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="f6c4d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6c4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c4d-110">*PropertyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6c4d-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c4d-111">Especifica a propriedade de política que o método está configurando.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-111">Specifies the policy property that the method is setting.</span></span>

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span data-ttu-id="f6c4d-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="f6c4d-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="f6c4d-113">O método está definindo a propriedade **DeleteTempFolders** .</span><span class="sxs-lookup"><span data-stu-id="f6c4d-113">The method is setting the **DeleteTempFolders** property.</span></span>

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span data-ttu-id="f6c4d-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="f6c4d-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="f6c4d-115">O método está definindo a propriedade **UseTempFolders** .</span><span class="sxs-lookup"><span data-stu-id="f6c4d-115">The method is setting the **UseTempFolders** property.</span></span>

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span data-ttu-id="f6c4d-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Ajuda**</span><span class="sxs-lookup"><span data-stu-id="f6c4d-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Help**</span></span>


</dt> <dd>

<span data-ttu-id="f6c4d-117">O método está definindo a propriedade da **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="f6c4d-117">The method is setting the **Help** property.</span></span>

<span data-ttu-id="f6c4d-118">**Observação** não há suporte para **a ajuda**  </span><span class="sxs-lookup"><span data-stu-id="f6c4d-118">**Note**  **Help** is not supported</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f6c4d-119">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f6c4d-119">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c4d-120">Valor que indica se a propriedade especificada pelo parâmetro *PropertyName* deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-120">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="f6c4d-121"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="f6c4d-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="f6c4d-122">Desabilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-122">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="f6c4d-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f6c4d-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f6c4d-124">Habilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-124">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c4d-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6c4d-125">Return value</span></span>

<span data-ttu-id="f6c4d-126">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f6c4d-127">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="f6c4d-128">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6c4d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6c4d-129">Remarks</span></span>

<span data-ttu-id="f6c4d-130">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f6c4d-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f6c4d-131">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f6c4d-132">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f6c4d-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f6c4d-133">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f6c4d-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c4d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6c4d-134">Requirements</span></span>



| <span data-ttu-id="f6c4d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6c4d-135">Requirement</span></span> | <span data-ttu-id="f6c4d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="f6c4d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c4d-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c4d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c4d-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6c4d-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6c4d-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c4d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c4d-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6c4d-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6c4d-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6c4d-141">Namespace</span></span><br/>                | <span data-ttu-id="f6c4d-142">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f6c4d-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f6c4d-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f6c4d-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6c4d-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6c4d-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6c4d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f6c4d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6c4d-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6c4d-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6c4d-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6c4d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6c4d-148">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f6c4d-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

