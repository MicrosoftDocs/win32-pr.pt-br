---
title: Método SetHomeDirectory da classe Win32_TerminalServiceSetting
description: Define a propriedade TerminalServicesHomeDirectory para a classe.
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetHomeDirectory
- Método SetHomeDirectory Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetHomeDirectory
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499341"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="e777f-106">Método SetHomeDirectory da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="e777f-106">SetHomeDirectory method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="e777f-107">O método **SetHomeDirectory** define a propriedade **TerminalServicesHomeDirectory** para a classe.</span><span class="sxs-lookup"><span data-stu-id="e777f-107">The **SetHomeDirectory** method sets the **TerminalServicesHomeDirectory** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="e777f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e777f-108">Syntax</span></span>


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="e777f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e777f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e777f-110">*HomeDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e777f-110">*HomeDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e777f-111">O novo valor para a propriedade **TerminalServicesHomeDirectory** , que especifica o diretório raiz do computador.</span><span class="sxs-lookup"><span data-stu-id="e777f-111">The new value for the **TerminalServicesHomeDirectory** property, which specifies the computer's root directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e777f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e777f-112">Return value</span></span>

<span data-ttu-id="e777f-113">Retorna êxito em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="e777f-113">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="e777f-114">Para obter uma lista de códigos de erro do WMI, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e777f-114">For a list of WMI error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e777f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e777f-115">Remarks</span></span>

<span data-ttu-id="e777f-116">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e777f-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e777f-117">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e777f-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e777f-118">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e777f-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e777f-119">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e777f-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e777f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e777f-120">Requirements</span></span>



| <span data-ttu-id="e777f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e777f-121">Requirement</span></span> | <span data-ttu-id="e777f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e777f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e777f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e777f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e777f-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e777f-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e777f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e777f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e777f-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e777f-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e777f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="e777f-127">Namespace</span></span><br/>                | <span data-ttu-id="e777f-128">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e777f-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e777f-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e777f-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e777f-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e777f-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e777f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e777f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e777f-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e777f-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e777f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e777f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e777f-134">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="e777f-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

