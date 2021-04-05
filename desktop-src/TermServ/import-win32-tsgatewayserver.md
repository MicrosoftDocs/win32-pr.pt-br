---
title: Método de importação da classe Win32_TSGatewayServer
description: Importa uma determinada configuração para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Método de importação Serviços de Área de Trabalho Remota
- Método de importação Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServer
- Classe de Win32_TSGatewayServer Serviços de Área de Trabalho Remota, método de importação
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918659"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="35020-106">Método de importação da \_ classe Win32 TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="35020-106">Import method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="35020-107">Importa uma determinada configuração para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="35020-107">Imports a given configuration to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="35020-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35020-108">Syntax</span></span>


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a><span data-ttu-id="35020-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35020-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35020-110">*ImportType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35020-110">*ImportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35020-111">O conteúdo a ser importado.</span><span class="sxs-lookup"><span data-stu-id="35020-111">The content to import.</span></span> <span data-ttu-id="35020-112">Defina o tipo de importação definindo os bits correspondentes no parâmetro *importType* .</span><span class="sxs-lookup"><span data-stu-id="35020-112">Set the import type by setting the corresponding bits in the *ImportType* parameter.</span></span> <span data-ttu-id="35020-113">Você pode definir vários tipos de importação.</span><span class="sxs-lookup"><span data-stu-id="35020-113">You can set multiple import types.</span></span> <span data-ttu-id="35020-114">Por exemplo, se o 0 bit for definido, Serviços de Área de Trabalho Remota RD CAPs (políticas de autorização de conexão) serão importadas.</span><span class="sxs-lookup"><span data-stu-id="35020-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be imported.</span></span> <span data-ttu-id="35020-115">Se 0 e o 2º bit forem definidos, as RD CAPs Serviços de Área de Trabalho Remota e as RD RAPs (políticas de autorização de recursos) serão importadas.</span><span class="sxs-lookup"><span data-stu-id="35020-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be imported.</span></span>

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span data-ttu-id="35020-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importar todas as tampas** (1)</span><span class="sxs-lookup"><span data-stu-id="35020-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Import all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="35020-117">Importar todas as RD CAPs.</span><span class="sxs-lookup"><span data-stu-id="35020-117">Import all RD CAPs.</span></span>

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="35020-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importar todos os servidores RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="35020-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Import all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="35020-119">Importe uma lista de todos os servidores de servidor de diretivas de rede (NPS).</span><span class="sxs-lookup"><span data-stu-id="35020-119">Import a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span data-ttu-id="35020-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importar todas as raps** (4)</span><span class="sxs-lookup"><span data-stu-id="35020-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Import all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="35020-121">Importar todas as RD RAPs.</span><span class="sxs-lookup"><span data-stu-id="35020-121">Import all RD RAPs.</span></span>

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span data-ttu-id="35020-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importar todos os RGS** (8)</span><span class="sxs-lookup"><span data-stu-id="35020-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Import all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="35020-123">Importar todos os grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="35020-123">Import all resource groups.</span></span>

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="35020-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importar todos os servidores de balanceamento de carga** (16)</span><span class="sxs-lookup"><span data-stu-id="35020-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Import all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="35020-125">Importe uma lista de todos os servidores de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="35020-125">Import a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="35020-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importar todas as configurações do servidor** (32)</span><span class="sxs-lookup"><span data-stu-id="35020-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Import all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="35020-127">Importar todas as configurações de servidor relacionadas ao gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="35020-127">Import all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="35020-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importar todas as políticas de integridade** (64)</span><span class="sxs-lookup"><span data-stu-id="35020-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Import all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="35020-129">Importar todas as políticas de integridade.</span><span class="sxs-lookup"><span data-stu-id="35020-129">Import all health policies.</span></span>

<span data-ttu-id="35020-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="35020-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="35020-131">Não há suporte para esse valor antes do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="35020-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="35020-132">*XmlString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35020-132">*XmlString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35020-133">A configuração como uma cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="35020-133">The configuration as an XML string.</span></span>

</dd> <dt>

<span data-ttu-id="35020-134">*MergeOrReplace* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35020-134">*MergeOrReplace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35020-135">Indica se os dados devem ser mesclados ou substituídos quando ocorre um conflito.</span><span class="sxs-lookup"><span data-stu-id="35020-135">Indicates whether to merge or replace data when a conflict occurs.</span></span>

> [!Note]  
> <span data-ttu-id="35020-136">A mesclagem ainda não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="35020-136">Merge is not yet implemented.</span></span> <span data-ttu-id="35020-137">Portanto, esse valor de parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="35020-137">Therefore, this parameter value is ignored.</span></span>

 

</dd> <dt>

<span data-ttu-id="35020-138">*LogString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="35020-138">*LogString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35020-139">As informações de log geradas durante a operação de importação.</span><span class="sxs-lookup"><span data-stu-id="35020-139">The log information that is generated during the import operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35020-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="35020-140">Remarks</span></span>

<span data-ttu-id="35020-141">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="35020-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="35020-142">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="35020-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="35020-143">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="35020-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="35020-144">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="35020-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="35020-145">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="35020-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="35020-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35020-146">Requirements</span></span>



| <span data-ttu-id="35020-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="35020-147">Requirement</span></span> | <span data-ttu-id="35020-148">Valor</span><span class="sxs-lookup"><span data-stu-id="35020-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35020-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35020-149">Minimum supported client</span></span><br/> | <span data-ttu-id="35020-150">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="35020-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="35020-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35020-151">Minimum supported server</span></span><br/> | <span data-ttu-id="35020-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35020-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="35020-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="35020-153">Namespace</span></span><br/>                | <span data-ttu-id="35020-154">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="35020-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="35020-155">MOF</span><span class="sxs-lookup"><span data-stu-id="35020-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35020-156"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35020-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="35020-157">DLL</span><span class="sxs-lookup"><span data-stu-id="35020-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35020-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35020-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="35020-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="35020-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35020-160">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="35020-160">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

