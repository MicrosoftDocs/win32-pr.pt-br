---
title: Método IsLSPreventUpgradeGPEnabled da classe Win32_TSLicenseServer
description: Recupera se o \ 0034; impede a atualização da licença \ 0034; a configuração de política de grupo está habilitada no servidor de licença Área de Trabalho Remota.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsLSPreventUpgradeGPEnabled
- Método IsLSPreventUpgradeGPEnabled Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsLSPreventUpgradeGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754709"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="bae9d-106">Método IsLSPreventUpgradeGPEnabled da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="bae9d-106">IsLSPreventUpgradeGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="bae9d-107">Recupera se a configuração da política de grupo "impedir atualização de licença" está habilitada no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="bae9d-107">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae9d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bae9d-108">Syntax</span></span>


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="bae9d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bae9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bae9d-110">*Habilitado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bae9d-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bae9d-111">Valor booliano que indica se a configuração de política "impedir atualização de licença" está habilitada.</span><span class="sxs-lookup"><span data-stu-id="bae9d-111">Boolean value that indicates whether the "prevent license upgrade" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bae9d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bae9d-112">Return value</span></span>

<span data-ttu-id="bae9d-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="bae9d-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bae9d-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="bae9d-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bae9d-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bae9d-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bae9d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bae9d-116">Remarks</span></span>

<span data-ttu-id="bae9d-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="bae9d-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bae9d-118">Se a configuração de política "impedir atualização de licença" estiver habilitada, o servidor de licença emitirá apenas um RDS CAL temporário para o cliente se um RDS CAL apropriado para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="bae9d-118">If the "prevent license upgrade" policy setting is enabled, the license server will only issue a temporary RDS CAL to the client if an appropriate RDS CAL for the Remote Desktop Session Host (RD Session Host) server is not available.</span></span>

<span data-ttu-id="bae9d-119">A configuração de política está localizada no seguinte nó do editor de diretiva de grupo local:</span><span class="sxs-lookup"><span data-stu-id="bae9d-119">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="bae9d-120">Configuração do computador \\ modelos administrativos \\ componentes do Windows \\ \\ Licenciamento TS dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="bae9d-120">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="bae9d-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bae9d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bae9d-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bae9d-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bae9d-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="bae9d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bae9d-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bae9d-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bae9d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bae9d-125">Requirements</span></span>



| <span data-ttu-id="bae9d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bae9d-126">Requirement</span></span> | <span data-ttu-id="bae9d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bae9d-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae9d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bae9d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bae9d-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bae9d-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="bae9d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bae9d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bae9d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bae9d-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="bae9d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="bae9d-132">Namespace</span></span><br/>                | <span data-ttu-id="bae9d-133">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="bae9d-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="bae9d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bae9d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bae9d-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bae9d-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bae9d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bae9d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bae9d-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bae9d-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bae9d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bae9d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae9d-139">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="bae9d-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

