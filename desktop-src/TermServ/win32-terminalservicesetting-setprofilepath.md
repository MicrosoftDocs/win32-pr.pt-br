---
title: Método SetProfilePath da classe Win32_TerminalServiceSetting
description: O método SetProfilePath define a propriedade ProfilePath para a classe.
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetProfilePath
- Método SetProfilePath Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetProfilePath
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 434909471accc191e79c92287ab6e4ac427bf949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369558"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="8a24e-106">Método SetProfilePath da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="8a24e-106">SetProfilePath method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="8a24e-107">O método **SetProfilePath** define a propriedade **ProfilePath** para a classe.</span><span class="sxs-lookup"><span data-stu-id="8a24e-107">The **SetProfilePath** method sets the **ProfilePath** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a24e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a24e-108">Syntax</span></span>


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a><span data-ttu-id="8a24e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a24e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a24e-110">*ProfilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a24e-110">*ProfilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a24e-111">O novo valor para a propriedade **ProfilePath** , que especifica o caminho do perfil para o computador.</span><span class="sxs-lookup"><span data-stu-id="8a24e-111">The new value for the **ProfilePath** property, which specifies the profile path for the computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a24e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a24e-112">Return value</span></span>

<span data-ttu-id="8a24e-113">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="8a24e-113">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8a24e-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="8a24e-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a24e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a24e-115">Remarks</span></span>

<span data-ttu-id="8a24e-116">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8a24e-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8a24e-117">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8a24e-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8a24e-118">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="8a24e-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8a24e-119">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8a24e-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a24e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a24e-120">Requirements</span></span>



| <span data-ttu-id="8a24e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a24e-121">Requirement</span></span> | <span data-ttu-id="8a24e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8a24e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a24e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a24e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8a24e-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a24e-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a24e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a24e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8a24e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a24e-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a24e-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a24e-127">Namespace</span></span><br/>                | <span data-ttu-id="8a24e-128">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="8a24e-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8a24e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8a24e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a24e-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a24e-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a24e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8a24e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a24e-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a24e-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a24e-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8a24e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a24e-134">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8a24e-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

