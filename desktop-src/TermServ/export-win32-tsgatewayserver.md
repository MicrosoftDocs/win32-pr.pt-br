---
title: Método Export da classe Win32_TSGatewayServer
description: Retorna a configuração do servidor do gateway de Área de Trabalho Remota (Gateway RD) como uma cadeia de caracteres XML.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de exportação
- Método de exportação Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServer
- Classe de Win32_TSGatewayServer Serviços de Área de Trabalho Remota, método de exportação
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919211"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="22a1e-106">Método Export da classe Win32 \_ TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="22a1e-106">Export method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="22a1e-107">Retorna a configuração do servidor do gateway de Área de Trabalho Remota (Gateway RD) como uma cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="22a1e-107">Returns the Remote Desktop Gateway (RD Gateway) server configuration as an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a1e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22a1e-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a><span data-ttu-id="22a1e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22a1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a1e-110">*ExportType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="22a1e-110">*ExportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22a1e-111">O conteúdo a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="22a1e-111">The content to export.</span></span> <span data-ttu-id="22a1e-112">Defina o tipo de exportação definindo os bits correspondentes no parâmetro *ExportType* .</span><span class="sxs-lookup"><span data-stu-id="22a1e-112">Set the export type by setting the corresponding bits in the *ExportType* parameter.</span></span> <span data-ttu-id="22a1e-113">Você pode definir vários tipos de exportação.</span><span class="sxs-lookup"><span data-stu-id="22a1e-113">You can set multiple export types.</span></span> <span data-ttu-id="22a1e-114">Por exemplo, se o 0 bit for definido, Serviços de Área de Trabalho Remota RD CAPs (políticas de autorização de conexão) serão exportadas.</span><span class="sxs-lookup"><span data-stu-id="22a1e-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be exported.</span></span> <span data-ttu-id="22a1e-115">Se 0 e o 2º bit forem definidos, as RD CAPs Serviços de Área de Trabalho Remota e as RD RAPs (políticas de autorização de recursos) serão exportadas.</span><span class="sxs-lookup"><span data-stu-id="22a1e-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be exported.</span></span>

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span data-ttu-id="22a1e-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Exportar todas as tampas** (1)</span><span class="sxs-lookup"><span data-stu-id="22a1e-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Export all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="22a1e-117">Exportar todas as RD CAPs.</span><span class="sxs-lookup"><span data-stu-id="22a1e-117">Export all RD CAPs.</span></span>

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="22a1e-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Exportar todos os servidores RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="22a1e-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Export all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="22a1e-119">Exportar uma lista de todos os servidores de servidor de diretivas de rede (NPS).</span><span class="sxs-lookup"><span data-stu-id="22a1e-119">Export a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span data-ttu-id="22a1e-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Exportar todas as raps** (4)</span><span class="sxs-lookup"><span data-stu-id="22a1e-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Export all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="22a1e-121">Exportar todas as RD RAPs.</span><span class="sxs-lookup"><span data-stu-id="22a1e-121">Export all RD RAPs.</span></span>

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span data-ttu-id="22a1e-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Exportar todos os RGS** (8)</span><span class="sxs-lookup"><span data-stu-id="22a1e-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Export all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="22a1e-123">Exportar todos os grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="22a1e-123">Export all resource groups.</span></span>

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="22a1e-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Exportar todos os servidores de balanceamento de carga** (16)</span><span class="sxs-lookup"><span data-stu-id="22a1e-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Export all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="22a1e-125">Exportar uma lista de todos os servidores de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="22a1e-125">Export a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="22a1e-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Exportar todas as configurações do servidor** (32)</span><span class="sxs-lookup"><span data-stu-id="22a1e-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Export all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="22a1e-127">Exportar todas as configurações de servidor relacionadas ao gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="22a1e-127">Export all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="22a1e-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Exportar todas as políticas de integridade** (64)</span><span class="sxs-lookup"><span data-stu-id="22a1e-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Export all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="22a1e-129">Exportar todas as políticas de integridade.</span><span class="sxs-lookup"><span data-stu-id="22a1e-129">Export all health policies.</span></span>

<span data-ttu-id="22a1e-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="22a1e-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="22a1e-131">Não há suporte para esse valor antes do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="22a1e-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="22a1e-132">*XmlString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="22a1e-132">*XmlString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22a1e-133">A cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="22a1e-133">The XML string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22a1e-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="22a1e-134">Remarks</span></span>

<span data-ttu-id="22a1e-135">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="22a1e-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="22a1e-136">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="22a1e-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="22a1e-137">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="22a1e-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="22a1e-138">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="22a1e-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="22a1e-139">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="22a1e-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="22a1e-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22a1e-140">Requirements</span></span>



| <span data-ttu-id="22a1e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="22a1e-141">Requirement</span></span> | <span data-ttu-id="22a1e-142">Valor</span><span class="sxs-lookup"><span data-stu-id="22a1e-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a1e-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22a1e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="22a1e-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="22a1e-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="22a1e-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22a1e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="22a1e-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22a1e-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="22a1e-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="22a1e-147">Namespace</span></span><br/>                | <span data-ttu-id="22a1e-148">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="22a1e-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="22a1e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="22a1e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22a1e-150"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22a1e-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="22a1e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="22a1e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22a1e-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22a1e-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="22a1e-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="22a1e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a1e-154">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="22a1e-154">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

