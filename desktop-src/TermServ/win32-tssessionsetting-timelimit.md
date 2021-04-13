---
title: Método timelimite da classe Win32_TSSessionSetting
description: Define o tempo máximo alocado para o tipo de limite de sessão especificado.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método timelimite
- Método timelimite Serviços de Área de Trabalho Remota, classe Win32_TSSessionSetting
- Classe Win32_TSSessionSetting Serviços de Área de Trabalho Remota, método timelimite
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499247"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="9fb08-106">Método timelimite da classe Win32 \_ TSSessionSetting</span><span class="sxs-lookup"><span data-stu-id="9fb08-106">TimeLimit method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="9fb08-107">Define o tempo máximo alocado para o tipo de limite de sessão especificado.</span><span class="sxs-lookup"><span data-stu-id="9fb08-107">Sets the maximum time allocated to the specified session-limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb08-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fb08-108">Syntax</span></span>


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a><span data-ttu-id="9fb08-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fb08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb08-110">*SessionLimitType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fb08-110">*SessionLimitType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb08-111">Especifica o tipo de propriedade de limite de sessão que o método está configurando.</span><span class="sxs-lookup"><span data-stu-id="9fb08-111">Specifies the type of session-limit property that the method is setting.</span></span>

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span data-ttu-id="9fb08-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="9fb08-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="9fb08-113">O método está definindo a propriedade **ActiveSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="9fb08-113">The method is setting the **ActiveSessionLimit** property.</span></span>

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span data-ttu-id="9fb08-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="9fb08-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="9fb08-115">O método está definindo a propriedade **DisconnectedSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="9fb08-115">The method is setting the **DisconnectedSessionLimit** property.</span></span>

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span data-ttu-id="9fb08-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="9fb08-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="9fb08-117">O método está definindo a propriedade **IdleSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="9fb08-117">The method is setting the **IdleSessionLimit** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9fb08-118">*ValueLimit* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fb08-118">*ValueLimit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb08-119">O novo tempo máximo, em milissegundos, para a propriedade especificada pelo parâmetro *SessionLimitType* .</span><span class="sxs-lookup"><span data-stu-id="9fb08-119">The new maximum time, in milliseconds, for the property specified by the *SessionLimitType* parameter.</span></span> <span data-ttu-id="9fb08-120">O valor zero indica que não há limite de sessão.</span><span class="sxs-lookup"><span data-stu-id="9fb08-120">The value zero indicates that there is no session limit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb08-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9fb08-121">Return value</span></span>

<span data-ttu-id="9fb08-122">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="9fb08-122">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9fb08-123">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="9fb08-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="9fb08-124">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="9fb08-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb08-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fb08-125">Remarks</span></span>

<span data-ttu-id="9fb08-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9fb08-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9fb08-127">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9fb08-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9fb08-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9fb08-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9fb08-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9fb08-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fb08-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fb08-130">Requirements</span></span>



| <span data-ttu-id="9fb08-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb08-131">Requirement</span></span> | <span data-ttu-id="9fb08-132">Valor</span><span class="sxs-lookup"><span data-stu-id="9fb08-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb08-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb08-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb08-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fb08-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fb08-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb08-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb08-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fb08-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fb08-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fb08-137">Namespace</span></span><br/>                | <span data-ttu-id="9fb08-138">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9fb08-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9fb08-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9fb08-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fb08-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fb08-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fb08-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9fb08-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fb08-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fb08-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fb08-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fb08-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb08-144">**\_TSSessionSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="9fb08-144">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

