---
title: Método setclientproperty da classe Win32_TSClientSetting
description: O método setclientproperty define a propriedade LPTPortMapping, COMPortMapping, AudioMapping, ClipboardMapping, DriveMapping ou WindowsPrinterMapping para a classe.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- Método setclientproperty Serviços de Área de Trabalho Remota
- Método setclientproperty Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método setclientproperty
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754705"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="f22a8-106">Método setclientproperty da classe Win32 \_ TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="f22a8-106">SetClientProperty method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="f22a8-107">O **método Setclientproperty** define a propriedade **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** ou **WindowsPrinterMapping** para a classe.</span><span class="sxs-lookup"><span data-stu-id="f22a8-107">The **SetClientProperty** method sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="f22a8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f22a8-108">Syntax</span></span>


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="f22a8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f22a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f22a8-110">*PropertyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f22a8-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f22a8-111">Especifica a propriedade de cliente que o método está configurando.</span><span class="sxs-lookup"><span data-stu-id="f22a8-111">Specifies the client property that the method is setting.</span></span>

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span data-ttu-id="f22a8-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="f22a8-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span></span>


</dt> <dd>

<span data-ttu-id="f22a8-113">O método está definindo a propriedade **AudioMapping** .</span><span class="sxs-lookup"><span data-stu-id="f22a8-113">The method is setting the **AudioMapping** property.</span></span>

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span data-ttu-id="f22a8-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="f22a8-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span></span>


</dt> <dd>

<span data-ttu-id="f22a8-115">O método está definindo a propriedade **ClipboardMapping** .</span><span class="sxs-lookup"><span data-stu-id="f22a8-115">The method is setting the **ClipboardMapping** property.</span></span>

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span data-ttu-id="f22a8-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="f22a8-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="f22a8-117">O método está definindo a propriedade **COMPortMapping** .</span><span class="sxs-lookup"><span data-stu-id="f22a8-117">The method is setting the **COMPortMapping** property.</span></span>

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span data-ttu-id="f22a8-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="f22a8-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span></span>


</dt> <dd>

<span data-ttu-id="f22a8-119">O método está definindo a propriedade **DriveMapping** .</span><span class="sxs-lookup"><span data-stu-id="f22a8-119">The method is setting the **DriveMapping** property.</span></span>

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span data-ttu-id="f22a8-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="f22a8-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="f22a8-121">O método está definindo a propriedade **LPTPortMapping** .</span><span class="sxs-lookup"><span data-stu-id="f22a8-121">The method is setting the **LPTPortMapping** property.</span></span>

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span data-ttu-id="f22a8-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="f22a8-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span></span>


</dt> <dd>

<span data-ttu-id="f22a8-123">O método está definindo a propriedade **PNPRedirection** .</span><span class="sxs-lookup"><span data-stu-id="f22a8-123">The method is setting the **PNPRedirection** property.</span></span>

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span data-ttu-id="f22a8-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="f22a8-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span></span>


</dt> <dd>

<span data-ttu-id="f22a8-125">O método está definindo a propriedade **WindowsPrinterMapping** .</span><span class="sxs-lookup"><span data-stu-id="f22a8-125">The method is setting the **WindowsPrinterMapping** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f22a8-126">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f22a8-126">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f22a8-127">Valor que indica se a propriedade especificada pelo parâmetro *PropertyName* deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f22a8-127">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="f22a8-128"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="f22a8-128"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="f22a8-129">Desabilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="f22a8-129">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="f22a8-130"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f22a8-130"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f22a8-131">Habilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="f22a8-131">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f22a8-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f22a8-132">Return value</span></span>

<span data-ttu-id="f22a8-133">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="f22a8-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f22a8-134">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="f22a8-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="f22a8-135">O método retornará um erro se a propriedade de cliente especificada não estiver sob controle de diretiva de grupo ou se a configuração de propriedade não estiver qualificada para substituição pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="f22a8-135">The method returns an error if the specified client property is not under group policy control or if the property setting is not eligible for override by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="f22a8-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="f22a8-136">Remarks</span></span>

<span data-ttu-id="f22a8-137">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f22a8-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f22a8-138">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f22a8-138">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f22a8-139">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f22a8-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f22a8-140">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f22a8-140">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f22a8-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f22a8-141">Requirements</span></span>



| <span data-ttu-id="f22a8-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="f22a8-142">Requirement</span></span> | <span data-ttu-id="f22a8-143">Valor</span><span class="sxs-lookup"><span data-stu-id="f22a8-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f22a8-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f22a8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f22a8-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f22a8-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f22a8-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f22a8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f22a8-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f22a8-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f22a8-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="f22a8-148">Namespace</span></span><br/>                | <span data-ttu-id="f22a8-149">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f22a8-149">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f22a8-150">MOF</span><span class="sxs-lookup"><span data-stu-id="f22a8-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f22a8-151"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f22a8-151"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f22a8-152">DLL</span><span class="sxs-lookup"><span data-stu-id="f22a8-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f22a8-153"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f22a8-153"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f22a8-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="f22a8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22a8-155">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f22a8-155">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

