---
title: Método ExplicitLogon da classe Win32_TSLogonSetting
description: O método ExplicitLogon define as credenciais a serem usadas para autenticação.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ExplicitLogon
- Método ExplicitLogon Serviços de Área de Trabalho Remota, classe Win32_TSLogonSetting
- Classe Win32_TSLogonSetting Serviços de Área de Trabalho Remota, método ExplicitLogon
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369766"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="cde45-106">Método ExplicitLogon da classe Win32 \_ TSLogonSetting</span><span class="sxs-lookup"><span data-stu-id="cde45-106">ExplicitLogon method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="cde45-107">O método **ExplicitLogon** define as credenciais a serem usadas para autenticação.</span><span class="sxs-lookup"><span data-stu-id="cde45-107">The **ExplicitLogon** method sets the credentials to use for authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde45-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cde45-108">Syntax</span></span>


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a><span data-ttu-id="cde45-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cde45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cde45-110">*Nome de usuário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cde45-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde45-111">A credencial de logon do nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="cde45-111">The user name logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="cde45-112">*Domínio* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cde45-112">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde45-113">A credencial de logon de domínio.</span><span class="sxs-lookup"><span data-stu-id="cde45-113">The domain logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="cde45-114">*Senha* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cde45-114">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde45-115">A credencial de logon de senha.</span><span class="sxs-lookup"><span data-stu-id="cde45-115">The password logon credential.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cde45-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cde45-116">Return value</span></span>

<span data-ttu-id="cde45-117">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="cde45-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cde45-118">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="cde45-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="cde45-119">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="cde45-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="cde45-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="cde45-120">Remarks</span></span>

<span data-ttu-id="cde45-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cde45-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cde45-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cde45-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cde45-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="cde45-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cde45-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cde45-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cde45-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cde45-125">Requirements</span></span>



| <span data-ttu-id="cde45-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde45-126">Requirement</span></span> | <span data-ttu-id="cde45-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cde45-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cde45-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cde45-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cde45-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cde45-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cde45-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cde45-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cde45-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cde45-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cde45-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="cde45-132">Namespace</span></span><br/>                | <span data-ttu-id="cde45-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="cde45-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cde45-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cde45-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cde45-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cde45-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cde45-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cde45-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde45-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde45-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cde45-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="cde45-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde45-139">**\_TSLogonSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cde45-139">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

