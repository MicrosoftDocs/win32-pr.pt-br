---
title: Método IsLSSecGrpGPEnabled da classe Win32_TSLicenseServer
description: Recupera se o grupo de segurança do servidor de licenças \ 0034; \ 0034; a configuração de política de grupo está habilitada no servidor de licença Área de Trabalho Remota.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsLSSecGrpGPEnabled
- Método IsLSSecGrpGPEnabled Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsLSSecGrpGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085763"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="cd344-106">Método IsLSSecGrpGPEnabled da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="cd344-106">IsLSSecGrpGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="cd344-107">Recupera se a configuração da política de grupo "grupo de segurança do servidor de licenças" está habilitada no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="cd344-107">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd344-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd344-108">Syntax</span></span>


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="cd344-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd344-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd344-110">*Habilitado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cd344-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd344-111">Valor booliano que indica se a configuração de política "grupo de segurança de servidor de licenças" está habilitada.</span><span class="sxs-lookup"><span data-stu-id="cd344-111">Boolean value that indicates whether the "license server security group" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd344-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd344-112">Return value</span></span>

<span data-ttu-id="cd344-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="cd344-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cd344-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="cd344-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cd344-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cd344-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd344-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd344-116">Remarks</span></span>

<span data-ttu-id="cd344-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="cd344-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="cd344-118">A configuração de política "grupo de segurança de servidor de licenças" permite que você especifique os servidores de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) que têm permissão para contatar o servidor de licença para obter Serviços de Área de Trabalho Remota CALs (licenças de acesso para cliente).</span><span class="sxs-lookup"><span data-stu-id="cd344-118">The "license server security group" policy setting allows you to specify the Remote Desktop Session Host (RD Session Host) servers that are permitted to contact the license server to obtain Remote Desktop Services client access licenses (RDS CALs).</span></span> <span data-ttu-id="cd344-119">Se a configuração de política estiver habilitada no servidor de licença, o servidor responderá apenas a solicitações de RDS CAL de Host da Sessão RD servidores cujas contas de computador são membros do grupo local computadores Terminal Server no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="cd344-119">If the policy setting is enabled on the license server, the server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="cd344-120">A configuração de política está localizada no seguinte nó do editor de diretiva de grupo local:</span><span class="sxs-lookup"><span data-stu-id="cd344-120">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="cd344-121">Configuração do computador \\ modelos administrativos \\ componentes do Windows \\ \\ Licenciamento TS dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="cd344-121">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="cd344-122">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cd344-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cd344-123">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cd344-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cd344-124">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="cd344-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cd344-125">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cd344-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd344-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd344-126">Requirements</span></span>



| <span data-ttu-id="cd344-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd344-127">Requirement</span></span> | <span data-ttu-id="cd344-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cd344-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd344-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd344-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cd344-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cd344-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="cd344-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd344-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cd344-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd344-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="cd344-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd344-133">Namespace</span></span><br/>                | <span data-ttu-id="cd344-134">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="cd344-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="cd344-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cd344-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd344-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd344-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd344-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cd344-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd344-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd344-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd344-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd344-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd344-140">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="cd344-140">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

