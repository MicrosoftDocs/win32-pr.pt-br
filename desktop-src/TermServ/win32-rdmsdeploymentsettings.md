---
title: Classe Win32_RDMSDeploymentSettings
description: Gerencia configurações de implantação para uma coleção de áreas de trabalho virtuais.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSDeploymentSettings Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSDeploymentSettings classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499323"
---
# <a name="win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="b5d78-105">\_Classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="b5d78-105">Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="b5d78-106">Gerencia configurações de implantação para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5d78-106">Manages deployment settings for a virtual desktop collection.</span></span>

<span data-ttu-id="b5d78-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b5d78-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d78-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5d78-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a><span data-ttu-id="b5d78-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b5d78-109">Members</span></span>

<span data-ttu-id="b5d78-110">A classe **Win32 \_ RDMSDeploymentSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b5d78-110">The **Win32\_RDMSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="b5d78-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b5d78-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b5d78-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b5d78-112">Methods</span></span>

<span data-ttu-id="b5d78-113">A classe **Win32 \_ RDMSDeploymentSettings** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b5d78-113">The **Win32\_RDMSDeploymentSettings** class has these methods.</span></span>



| <span data-ttu-id="b5d78-114">Método</span><span class="sxs-lookup"><span data-stu-id="b5d78-114">Method</span></span>                                                                                                  | <span data-ttu-id="b5d78-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5d78-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5d78-116">**GetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="b5d78-116">**GetBaseVHDPath**</span></span>](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="b5d78-117">Recupera o caminho base para o diretório no qual os VHDs do conjunto de áreas de trabalho virtuais são implantados.</span><span class="sxs-lookup"><span data-stu-id="b5d78-117">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="b5d78-118">**GetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="b5d78-118">**GetConnectionString**</span></span>](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | <span data-ttu-id="b5d78-119">Recupera a cadeia de conexão do banco de dados de nível de implantação.</span><span class="sxs-lookup"><span data-stu-id="b5d78-119">Retrieves the deployment-level database connection string.</span></span><br/>                                                             |
| [<span data-ttu-id="b5d78-120">**GetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="b5d78-120">**GetDiffVHDPath**</span></span>](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="b5d78-121">Recupera o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5d78-121">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>            |
| [<span data-ttu-id="b5d78-122">**GetExportPath**</span><span class="sxs-lookup"><span data-stu-id="b5d78-122">**GetExportPath**</span></span>](getexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="b5d78-123">Recupera o caminho do diretório para o qual as máquinas virtuais são implantadas para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5d78-123">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                  |
| [<span data-ttu-id="b5d78-124">**Getint32property**</span><span class="sxs-lookup"><span data-stu-id="b5d78-124">**GetInt32Property**</span></span>](getint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="b5d78-125">Recupera uma propriedade de número inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b5d78-125">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                             |
| [<span data-ttu-id="b5d78-126">**GetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="b5d78-126">**GetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | <span data-ttu-id="b5d78-127">Recupera a cadeia de conexão secundária do banco de dados no nível da implantação, que pode ser usada para dar suporte à expiração da senha.</span><span class="sxs-lookup"><span data-stu-id="b5d78-127">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span><br/> |
| [<span data-ttu-id="b5d78-128">**GetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="b5d78-128">**GetSMBPath**</span></span>](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="b5d78-129">Recupera o caminho UNC para o compartilhamento SMB no qual as máquinas virtuais do conjunto de áreas de trabalho virtuais são implantadas.</span><span class="sxs-lookup"><span data-stu-id="b5d78-129">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>      |
| [<span data-ttu-id="b5d78-130">**GetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="b5d78-130">**GetStringArrayDeploymentSetting**</span></span>](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="b5d78-131">Recupera as configurações de implantação para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5d78-131">Retrieves the deployment settings for a virtual desktop collection.</span></span><br/>                                                    |
| [<span data-ttu-id="b5d78-132">**Getstringproperty**</span><span class="sxs-lookup"><span data-stu-id="b5d78-132">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="b5d78-133">Recupera uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b5d78-133">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="b5d78-134">**RemoveDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="b5d78-134">**RemoveDeploymentSetting**</span></span>](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | <span data-ttu-id="b5d78-135">Exclui as configurações de implantação para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5d78-135">Deletes the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="b5d78-136">**SetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="b5d78-136">**SetBaseVHDPath**</span></span>](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="b5d78-137">Recupera o caminho base para o diretório no qual os VHDs do conjunto de áreas de trabalho virtuais são implantados.</span><span class="sxs-lookup"><span data-stu-id="b5d78-137">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="b5d78-138">**SetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="b5d78-138">**SetConnectionString**</span></span>](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | <span data-ttu-id="b5d78-139">Define a cadeia de conexão do banco de dados de nível de implantação.</span><span class="sxs-lookup"><span data-stu-id="b5d78-139">Sets the deployment-level database connection string.</span></span><br/>                                                                  |
| [<span data-ttu-id="b5d78-140">**SetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="b5d78-140">**SetDiffVHDPath**</span></span>](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="b5d78-141">Atualiza o caminho do diretório para o qual os discos diferenciais são implantados para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5d78-141">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>              |
| [<span data-ttu-id="b5d78-142">**SetExportPath**</span><span class="sxs-lookup"><span data-stu-id="b5d78-142">**SetExportPath**</span></span>](setexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="b5d78-143">Atualiza o caminho do diretório para o qual as máquinas virtuais são implantadas para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5d78-143">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                    |
| [<span data-ttu-id="b5d78-144">**Setint32property**</span><span class="sxs-lookup"><span data-stu-id="b5d78-144">**SetInt32Property**</span></span>](setint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="b5d78-145">Atualiza uma propriedade de inteiro para as configurações de implantação de uma coleção de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b5d78-145">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="b5d78-146">**SetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="b5d78-146">**SetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | <span data-ttu-id="b5d78-147">Define a cadeia de conexão secundária do banco de dados no nível da implantação.</span><span class="sxs-lookup"><span data-stu-id="b5d78-147">Sets the deployment-level database secondary connection string.</span></span><br/>                                                        |
| [<span data-ttu-id="b5d78-148">**SetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="b5d78-148">**SetSMBPath**</span></span>](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="b5d78-149">Atualiza o caminho UNC para o compartilhamento SMB no qual as máquinas virtuais do conjunto de áreas de trabalho virtuais são implantadas.</span><span class="sxs-lookup"><span data-stu-id="b5d78-149">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>        |
| [<span data-ttu-id="b5d78-150">**SetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="b5d78-150">**SetStringArrayDeploymentSetting**</span></span>](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="b5d78-151">Atualiza as configurações de implantação para uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5d78-151">Updates the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="b5d78-152">**Setstringproperty**</span><span class="sxs-lookup"><span data-stu-id="b5d78-152">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="b5d78-153">Atualiza uma propriedade de cadeia de caracteres para as configurações de implantação de uma coleção de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b5d78-153">Updates a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="b5d78-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5d78-154">Requirements</span></span>



| <span data-ttu-id="b5d78-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5d78-155">Requirement</span></span> | <span data-ttu-id="b5d78-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b5d78-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d78-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5d78-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d78-158">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b5d78-158">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b5d78-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5d78-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d78-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5d78-160">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b5d78-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5d78-161">Namespace</span></span><br/>                | <span data-ttu-id="b5d78-162">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="b5d78-162">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b5d78-163">MOF</span><span class="sxs-lookup"><span data-stu-id="b5d78-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5d78-164"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5d78-164"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5d78-165">DLL</span><span class="sxs-lookup"><span data-stu-id="b5d78-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5d78-166"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5d78-166"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b5d78-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5d78-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d78-168">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="b5d78-168">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





