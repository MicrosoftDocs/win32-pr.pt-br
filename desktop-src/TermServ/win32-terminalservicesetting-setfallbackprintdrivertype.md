---
title: Método SetFallbackPrintDriverType da classe Win32_TerminalServiceSetting
description: O método SetFallbackPrintDriverType define a propriedade FallbackPrintDriverType para a classe.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetFallbackPrintDriverType
- Método SetFallbackPrintDriverType Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetFallbackPrintDriverType
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009690"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="9fc90-106">Método SetFallbackPrintDriverType da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="9fc90-106">SetFallbackPrintDriverType method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="9fc90-107">O método **SetFallbackPrintDriverType** define a propriedade **FallbackPrintDriverType** para a classe.</span><span class="sxs-lookup"><span data-stu-id="9fc90-107">The **SetFallbackPrintDriverType** method sets the **FallbackPrintDriverType** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc90-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fc90-108">Syntax</span></span>


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a><span data-ttu-id="9fc90-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fc90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc90-110">*FallbackPrintDriverType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fc90-110">*FallbackPrintDriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc90-111">Define a propriedade **FallbackPrintDriverType** que permite ou nega novas conexões serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="9fc90-111">Sets the **FallbackPrintDriverType** property which allows or denies new Remote Desktop Services connections.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9fc90-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="9fc90-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9fc90-113">Nenhum driver de fallback.</span><span class="sxs-lookup"><span data-stu-id="9fc90-113">No fallback drivers.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9fc90-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9fc90-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9fc90-115">Melhor estimativa.</span><span class="sxs-lookup"><span data-stu-id="9fc90-115">Best guess.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="9fc90-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="9fc90-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="9fc90-117">Melhor estimativa.</span><span class="sxs-lookup"><span data-stu-id="9fc90-117">Best guess.</span></span> <span data-ttu-id="9fc90-118">Se nenhuma correspondência for encontrada, fallback para Hewlett-Packard PCL (linguagem de controle de impressora).</span><span class="sxs-lookup"><span data-stu-id="9fc90-118">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="9fc90-119"><span id="3"></span>**Beta**</span><span class="sxs-lookup"><span data-stu-id="9fc90-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="9fc90-120">Melhor estimativa.</span><span class="sxs-lookup"><span data-stu-id="9fc90-120">Best guess.</span></span> <span data-ttu-id="9fc90-121">Se nenhuma correspondência for encontrada, fallback para o PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="9fc90-121">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="9fc90-122"><span id="4"></span>**quatro**</span><span class="sxs-lookup"><span data-stu-id="9fc90-122"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="9fc90-123">Melhor estimativa.</span><span class="sxs-lookup"><span data-stu-id="9fc90-123">Best guess.</span></span> <span data-ttu-id="9fc90-124">Se nenhuma correspondência for encontrada, mostre os drivers PS e PCL.</span><span class="sxs-lookup"><span data-stu-id="9fc90-124">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc90-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9fc90-125">Return value</span></span>

<span data-ttu-id="9fc90-126">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="9fc90-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9fc90-127">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="9fc90-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="9fc90-128">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="9fc90-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc90-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fc90-129">Remarks</span></span>

<span data-ttu-id="9fc90-130">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9fc90-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9fc90-131">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9fc90-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9fc90-132">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9fc90-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9fc90-133">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9fc90-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc90-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fc90-134">Requirements</span></span>



| <span data-ttu-id="9fc90-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fc90-135">Requirement</span></span> | <span data-ttu-id="9fc90-136">Valor</span><span class="sxs-lookup"><span data-stu-id="9fc90-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc90-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fc90-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc90-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fc90-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fc90-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fc90-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc90-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fc90-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fc90-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fc90-141">Namespace</span></span><br/>                | <span data-ttu-id="9fc90-142">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9fc90-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9fc90-143">MOF</span><span class="sxs-lookup"><span data-stu-id="9fc90-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fc90-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fc90-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fc90-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9fc90-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fc90-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc90-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc90-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fc90-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc90-148">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="9fc90-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

