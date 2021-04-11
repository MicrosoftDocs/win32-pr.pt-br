---
title: Método SetUserAuthenticationRequired da classe Win32_TSGeneralSetting
description: Habilita ou desabilita o requisito de que os usuários devem ser autenticados no momento da conexão, definindo o valor da propriedade UserAuthenticationRequired.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetUserAuthenticationRequired
- Método SetUserAuthenticationRequired Serviços de Área de Trabalho Remota, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Serviços de Área de Trabalho Remota, método SetUserAuthenticationRequired
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295874"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="5328d-106">Método SetUserAuthenticationRequired da classe Win32 \_ TSGeneralSetting</span><span class="sxs-lookup"><span data-stu-id="5328d-106">SetUserAuthenticationRequired method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="5328d-107">Habilita ou desabilita o requisito de que os usuários devem ser autenticados no momento da conexão, definindo o valor da propriedade **UserAuthenticationRequired** na classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="5328d-107">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property in the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span> <span data-ttu-id="5328d-108">Se **for true**, o que significa habilitado, o **UserAuthenticationRequired** exigirá a autenticação do usuário no momento da conexão para aumentar a proteção do servidor contra ataques à rede.</span><span class="sxs-lookup"><span data-stu-id="5328d-108">If **True**, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="5328d-109">Somente clientes protocolo RDP (RDP) que oferecem suporte a RDP versão 6,0 ou superior são capazes de se conectar.</span><span class="sxs-lookup"><span data-stu-id="5328d-109">Only Remote Desktop Protocol (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="5328d-110">Para evitar interrupções para usuários remotos, é recomendável implantar clientes RDP que dão suporte à versão de protocolo apropriada antes de habilitar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="5328d-110">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5328d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5328d-111">Syntax</span></span>


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a><span data-ttu-id="5328d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5328d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5328d-113">*UserAuthenticationRequired* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5328d-113">*UserAuthenticationRequired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5328d-114">Indica se a autenticação do usuário é necessária.</span><span class="sxs-lookup"><span data-stu-id="5328d-114">Indicates whether user authentication is required.</span></span>

<dt>

<span data-ttu-id="5328d-115">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="5328d-115">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="5328d-116">Desabilitar o requisito de que o usuário deve ser autenticado</span><span class="sxs-lookup"><span data-stu-id="5328d-116">Disable requirement that user must be authenticated</span></span>

</dd> <dt>

<span data-ttu-id="5328d-117">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5328d-117">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="5328d-118">Habilita o requisito de que o usuário deve ser autenticado.</span><span class="sxs-lookup"><span data-stu-id="5328d-118">Enables requirement that user must be authenticated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5328d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5328d-119">Return value</span></span>

<span data-ttu-id="5328d-120">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="5328d-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5328d-121">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="5328d-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5328d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="5328d-122">Remarks</span></span>

<span data-ttu-id="5328d-123">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5328d-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5328d-124">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5328d-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5328d-125">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="5328d-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5328d-126">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5328d-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5328d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5328d-127">Requirements</span></span>



| <span data-ttu-id="5328d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5328d-128">Requirement</span></span> | <span data-ttu-id="5328d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5328d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5328d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5328d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5328d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5328d-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5328d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5328d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5328d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5328d-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5328d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="5328d-134">Namespace</span></span><br/>                | <span data-ttu-id="5328d-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="5328d-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5328d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5328d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5328d-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5328d-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5328d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5328d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5328d-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5328d-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5328d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="5328d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5328d-141">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="5328d-141">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

