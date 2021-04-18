---
title: Método EnvironmentVariables da classe Win32_TSExpandEnvironmentVariables
description: Expande variáveis de ambiente definidas pelo sistema. | Método EnvironmentVariables da classe Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnvironmentVariables
- Método EnvironmentVariables Serviços de Área de Trabalho Remota, classe Win32_TSExpandEnvironmentVariables
- Classe Win32_TSExpandEnvironmentVariables Serviços de Área de Trabalho Remota, método EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781025"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="62ea4-107">Método EnvironmentVariables da classe Win32 \_ TSExpandEnvironmentVariables</span><span class="sxs-lookup"><span data-stu-id="62ea4-107">EnvironmentVariables method of the Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="62ea4-108">Expande variáveis de ambiente definidas pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="62ea4-108">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ea4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62ea4-109">Syntax</span></span>


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a><span data-ttu-id="62ea4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62ea4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62ea4-111">*OriginalString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62ea4-111">*OriginalString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62ea4-112">Uma cadeia de caracteres que contém as variáveis de ambiente a serem expandidas.</span><span class="sxs-lookup"><span data-stu-id="62ea4-112">A string that contains the environment variables to expand.</span></span>

</dd> <dt>

<span data-ttu-id="62ea4-113">*Expandedstring* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="62ea4-113">*ExpandedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62ea4-114">Uma cadeia de caracteres com as variáveis de ambiente expandidas.</span><span class="sxs-lookup"><span data-stu-id="62ea4-114">A string with the environment variables expanded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62ea4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="62ea4-115">Remarks</span></span>

<span data-ttu-id="62ea4-116">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="62ea4-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="62ea4-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="62ea4-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="62ea4-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="62ea4-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="62ea4-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="62ea4-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="62ea4-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="62ea4-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="62ea4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62ea4-121">Requirements</span></span>



| <span data-ttu-id="62ea4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="62ea4-122">Requirement</span></span> | <span data-ttu-id="62ea4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="62ea4-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62ea4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62ea4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="62ea4-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="62ea4-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="62ea4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62ea4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="62ea4-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62ea4-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62ea4-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="62ea4-128">Namespace</span></span><br/>                | <span data-ttu-id="62ea4-129">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="62ea4-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="62ea4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="62ea4-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62ea4-131"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62ea4-131"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="62ea4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="62ea4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ea4-133"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ea4-133"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ea4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="62ea4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ea4-135">**\_TSExpandEnvironmentVariables Win32**</span><span class="sxs-lookup"><span data-stu-id="62ea4-135">**Win32\_TSExpandEnvironmentVariables**</span></span>](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

