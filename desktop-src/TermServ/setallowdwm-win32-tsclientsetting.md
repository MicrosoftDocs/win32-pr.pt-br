---
title: Método SetAllowDwm da classe Win32_TSClientSetting
description: Define a propriedade AllowDwm.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetAllowDwm
- Método SetAllowDwm Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método SetAllowDwm
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39441ba3244f206b057ba47c3cb6f765b5e80604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766943"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="4d06a-106">Método SetAllowDwm da classe Win32 \_ TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="4d06a-106">SetAllowDwm method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="4d06a-107">Define a propriedade **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="4d06a-107">Sets the **AllowDwm** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d06a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d06a-108">Syntax</span></span>


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a><span data-ttu-id="4d06a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d06a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d06a-110">*AllowDwm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d06a-110">*AllowDwm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d06a-111">O novo valor da propriedade **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="4d06a-111">The new **AllowDwm** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d06a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d06a-112">Return value</span></span>

<span data-ttu-id="4d06a-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="4d06a-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4d06a-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="4d06a-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="4d06a-115">O método retornará um erro se as configurações de conexão do usuário forem substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="4d06a-115">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d06a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d06a-116">Requirements</span></span>



| <span data-ttu-id="4d06a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d06a-117">Requirement</span></span> | <span data-ttu-id="4d06a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4d06a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d06a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d06a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d06a-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4d06a-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4d06a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d06a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d06a-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d06a-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="4d06a-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4d06a-123">End of client support</span></span><br/>    | <span data-ttu-id="4d06a-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4d06a-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4d06a-125">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4d06a-125">End of server support</span></span><br/>    | <span data-ttu-id="4d06a-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d06a-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="4d06a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d06a-127">Namespace</span></span><br/>                | <span data-ttu-id="4d06a-128">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="4d06a-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4d06a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4d06a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d06a-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d06a-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d06a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4d06a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d06a-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d06a-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d06a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d06a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d06a-134">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="4d06a-134">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





