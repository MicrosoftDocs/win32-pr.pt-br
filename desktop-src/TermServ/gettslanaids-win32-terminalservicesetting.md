---
title: Método GetTSLanaIds da classe Win32_TerminalServiceSetting
description: Obtém as IDs do adaptador de rede de área local (LANA) do NetBIOS e as descrições de Serviços de Área de Trabalho Remota adaptadores de rede.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetTSLanaIds
- Método GetTSLanaIds Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método GetTSLanaIds
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d2b2357df7e6d7ccc2cb8a774ba34c50cb46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456010"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="321f5-106">Método GetTSLanaIds da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="321f5-106">GetTSLanaIds method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="321f5-107">O método **GetTSLanaIds** Obtém as IDs do adaptador de rede de área local (Lana) do NetBIOS e as descrições de serviços de área de trabalho remota adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="321f5-107">The **GetTSLanaIds** method gets the NetBIOS Local Area Network Adapter (LANA) IDs and descriptions of Remote Desktop Services network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="321f5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="321f5-108">Syntax</span></span>


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="321f5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="321f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="321f5-110">*LanaIdList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="321f5-110">*LanaIdList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="321f5-111">Matriz de números de LANA.</span><span class="sxs-lookup"><span data-stu-id="321f5-111">Array of LANA numbers.</span></span>

</dd> <dt>

<span data-ttu-id="321f5-112">*LanaIdDescriptions* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="321f5-112">*LanaIdDescriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="321f5-113">Matriz de descrições de LANA correspondentes à matriz *LanaIdList* .</span><span class="sxs-lookup"><span data-stu-id="321f5-113">Array of LANA descriptions corresponding to the *LanaIdList* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="321f5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="321f5-114">Return value</span></span>

<span data-ttu-id="321f5-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="321f5-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="321f5-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="321f5-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="321f5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="321f5-117">Remarks</span></span>

<span data-ttu-id="321f5-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="321f5-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="321f5-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="321f5-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="321f5-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="321f5-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="321f5-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="321f5-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="321f5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="321f5-122">Requirements</span></span>



| <span data-ttu-id="321f5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="321f5-123">Requirement</span></span> | <span data-ttu-id="321f5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="321f5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="321f5-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="321f5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="321f5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="321f5-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="321f5-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="321f5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="321f5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="321f5-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="321f5-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="321f5-129">Namespace</span></span><br/>                | <span data-ttu-id="321f5-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="321f5-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="321f5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="321f5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="321f5-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="321f5-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="321f5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="321f5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="321f5-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="321f5-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321f5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="321f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321f5-136">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="321f5-136">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

