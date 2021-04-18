---
title: Método SetSingleSession da classe Win32_TerminalServiceSetting
description: O método SetSingleSession define a propriedade SingleSession para a classe.
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSingleSession
- Método SetSingleSession Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetSingleSession
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105799999"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="6af89-106">Método SetSingleSession da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="6af89-106">SetSingleSession method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="6af89-107">O método **SetSingleSession** define a propriedade **SingleSession** para a classe.</span><span class="sxs-lookup"><span data-stu-id="6af89-107">The **SetSingleSession** method sets the **SingleSession** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af89-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6af89-108">Syntax</span></span>


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a><span data-ttu-id="6af89-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6af89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af89-110">*SingleSession* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6af89-110">*SingleSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af89-111">Sinalizador desabilitando ou habilitando a propriedade **SingleSession** , que determina se os usuários estão limitados a uma ou mais sessões de serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="6af89-111">Flag disabling or enabling the **SingleSession** property, which determines whether users are limited to one or more Remote Desktop Services sessions.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="6af89-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="6af89-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="6af89-113">Desabilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="6af89-113">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="6af89-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="6af89-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="6af89-115">Habilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="6af89-115">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af89-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6af89-116">Return value</span></span>

<span data-ttu-id="6af89-117">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="6af89-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6af89-118">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="6af89-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af89-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6af89-119">Remarks</span></span>

<span data-ttu-id="6af89-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6af89-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6af89-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6af89-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6af89-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6af89-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6af89-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6af89-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6af89-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6af89-124">Requirements</span></span>



| <span data-ttu-id="6af89-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af89-125">Requirement</span></span> | <span data-ttu-id="6af89-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6af89-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6af89-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6af89-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6af89-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6af89-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6af89-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6af89-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6af89-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6af89-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6af89-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6af89-131">Namespace</span></span><br/>                | <span data-ttu-id="6af89-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6af89-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6af89-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6af89-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6af89-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6af89-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6af89-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6af89-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6af89-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6af89-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6af89-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6af89-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af89-138">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="6af89-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

