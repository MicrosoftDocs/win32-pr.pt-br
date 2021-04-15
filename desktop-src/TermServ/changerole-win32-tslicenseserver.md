---
title: Método ChangeRole da classe Win32_TSLicenseServer
description: Altera o escopo de descoberta do servidor de licença Área de Trabalho Remota. O escopo de descoberta determina quais servidores de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) na rede podem descobrir automaticamente o servidor de licença.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ChangeRole
- Método ChangeRole Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454839"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="d894f-107">Método ChangeRole da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="d894f-107">ChangeRole method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="d894f-108">Altera o escopo de descoberta do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="d894f-108">Changes the discovery scope of the Remote Desktop license server.</span></span> <span data-ttu-id="d894f-109">O escopo de descoberta determina quais servidores de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) na rede podem descobrir automaticamente o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="d894f-109">The discovery scope determines which Remote Desktop Session Host (RD Session Host) servers on the network can automatically discover the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d894f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d894f-110">Syntax</span></span>


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a><span data-ttu-id="d894f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d894f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d894f-112">*ServerRole* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d894f-112">*ServerRole* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d894f-113">Escopo de descoberta para o servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="d894f-113">Discovery scope for the Remote Desktop license server.</span></span> <span data-ttu-id="d894f-114">Você pode definir um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d894f-114">You can set one of the following values.</span></span>

<dt>

<span data-ttu-id="d894f-115">0</span><span class="sxs-lookup"><span data-stu-id="d894f-115">0</span></span>
</dt> <dd>

<span data-ttu-id="d894f-116">Host da Sessão RD servidores no mesmo grupo de trabalho podem descobrir o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="d894f-116">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="d894f-117">1</span><span class="sxs-lookup"><span data-stu-id="d894f-117">1</span></span>
</dt> <dd>

<span data-ttu-id="d894f-118">Host da Sessão RD servidores no mesmo domínio podem descobrir o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="d894f-118">RD Session Host servers in the same domain can discover the license server.</span></span> <span data-ttu-id="d894f-119">Você deve estar conectado como um administrador de domínio para definir esse valor.</span><span class="sxs-lookup"><span data-stu-id="d894f-119">You must be logged on as a domain administrator to set this value.</span></span>

</dd> <dt>

<span data-ttu-id="d894f-120">2</span><span class="sxs-lookup"><span data-stu-id="d894f-120">2</span></span>
</dt> <dd>

<span data-ttu-id="d894f-121">Host da Sessão RD servidores de vários domínios na mesma floresta podem descobrir o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="d894f-121">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span> <span data-ttu-id="d894f-122">Você deve estar conectado como um administrador corporativo para definir esse valor.</span><span class="sxs-lookup"><span data-stu-id="d894f-122">You must be logged on as an enterprise administrator to set this value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d894f-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d894f-123">Return value</span></span>

<span data-ttu-id="d894f-124">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="d894f-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d894f-125">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d894f-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d894f-126">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d894f-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d894f-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d894f-127">Remarks</span></span>

<span data-ttu-id="d894f-128">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="d894f-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d894f-129">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d894f-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d894f-130">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d894f-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d894f-131">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="d894f-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d894f-132">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d894f-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d894f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d894f-133">Requirements</span></span>



| <span data-ttu-id="d894f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d894f-134">Requirement</span></span> | <span data-ttu-id="d894f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d894f-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d894f-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d894f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d894f-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d894f-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d894f-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d894f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d894f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d894f-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d894f-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="d894f-140">Namespace</span></span><br/>                | <span data-ttu-id="d894f-141">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d894f-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d894f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d894f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d894f-143"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d894f-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d894f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d894f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d894f-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d894f-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d894f-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d894f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d894f-147">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="d894f-147">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

