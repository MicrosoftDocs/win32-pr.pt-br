---
title: Classe Win32_SessionBrokerServiceProperties
description: Define a consulta para um serviço de agente de sessão.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionBrokerServiceProperties classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499775"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="f80e3-105">\_Classe Win32 SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="f80e3-105">Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="f80e3-106">Define a consulta para um serviço de agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="f80e3-106">Defines the query for a session broker service.</span></span>

<span data-ttu-id="f80e3-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f80e3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f80e3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f80e3-108">Syntax</span></span>

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a><span data-ttu-id="f80e3-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f80e3-109">Members</span></span>

<span data-ttu-id="f80e3-110">A classe **Win32 \_ SessionBrokerServiceProperties** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f80e3-110">The **Win32\_SessionBrokerServiceProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="f80e3-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f80e3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f80e3-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f80e3-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="f80e3-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f80e3-113">Methods</span></span>

<span data-ttu-id="f80e3-114">A classe **Win32 \_ SessionBrokerServiceProperties** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f80e3-114">The **Win32\_SessionBrokerServiceProperties** class has these methods.</span></span>



| <span data-ttu-id="f80e3-115">Método</span><span class="sxs-lookup"><span data-stu-id="f80e3-115">Method</span></span>                                                                                                | <span data-ttu-id="f80e3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f80e3-116">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f80e3-117">**DeleteSBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="f80e3-117">**DeleteSBDbConnectionString**</span></span>](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | <span data-ttu-id="f80e3-118">Exclui cadeias de conexão de BD (primária e secundária) do registro.</span><span class="sxs-lookup"><span data-stu-id="f80e3-118">Deletes DB connection strings (primary and secondary) from the registry.</span></span><br/> <span data-ttu-id="f80e3-119">**Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Este método não está disponível antes do Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f80e3-119">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/> |
| [<span data-ttu-id="f80e3-120">**InstallBrokerDatabase**</span><span class="sxs-lookup"><span data-stu-id="f80e3-120">**InstallBrokerDatabase**</span></span>](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | <span data-ttu-id="f80e3-121">Instala o BD do agente de conexão RD no SQL Server central</span><span class="sxs-lookup"><span data-stu-id="f80e3-121">Installs RD Connection Broker DB on central SQL Server</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="f80e3-122">**IsDbReachable**</span><span class="sxs-lookup"><span data-stu-id="f80e3-122">**IsDbReachable**</span></span>](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | <span data-ttu-id="f80e3-123">Verifica se o BD está acessível</span><span class="sxs-lookup"><span data-stu-id="f80e3-123">Checks if DB is reachable</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="f80e3-124">**SetBrokerHAMode**</span><span class="sxs-lookup"><span data-stu-id="f80e3-124">**SetBrokerHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | <span data-ttu-id="f80e3-125">Migra dados do BD de WID local para o novo SQL Server DB baseado.</span><span class="sxs-lookup"><span data-stu-id="f80e3-125">Migrates data from local WID DB to the new SQL Server based DB.</span></span> <span data-ttu-id="f80e3-126">Ele também configura o servidor do agente para usar o SQL Server central</span><span class="sxs-lookup"><span data-stu-id="f80e3-126">It also configures the broker server to use the central SQL Server</span></span><br/>                                                                                        |
| [<span data-ttu-id="f80e3-127">**SetBrokerNonHAMode**</span><span class="sxs-lookup"><span data-stu-id="f80e3-127">**SetBrokerNonHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | <span data-ttu-id="f80e3-128">Migra dados do SQL Server central para o local DB.</span><span class="sxs-lookup"><span data-stu-id="f80e3-128">Migrates data from central SQL Server to local DB.</span></span> <span data-ttu-id="f80e3-129">Ele também configura o servidor do agente para usar o BD local.</span><span class="sxs-lookup"><span data-stu-id="f80e3-129">It also configures the broker server to use the local DB.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f80e3-130">**SetSBDbConnectionStrings**</span><span class="sxs-lookup"><span data-stu-id="f80e3-130">**SetSBDbConnectionStrings**</span></span>](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | <span data-ttu-id="f80e3-131">Salva as cadeias de conexão do BD (primária e secundária) no registro.</span><span class="sxs-lookup"><span data-stu-id="f80e3-131">Saves DB connection strings (primary and secondary) in the registry.</span></span><br/> <span data-ttu-id="f80e3-132">**Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Este método não está disponível antes do Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f80e3-132">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/>     |



 

### <a name="properties"></a><span data-ttu-id="f80e3-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f80e3-133">Properties</span></span>

<span data-ttu-id="f80e3-134">A classe **Win32 \_ SessionBrokerServiceProperties** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f80e3-134">The **Win32\_SessionBrokerServiceProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f80e3-135">**SBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="f80e3-135">**SBDbConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f80e3-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f80e3-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f80e3-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f80e3-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f80e3-138">Cadeia de conexão de banco de dados usada pelo serviço de agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="f80e3-138">Database connection string used by Session Broker service.</span></span>

<span data-ttu-id="f80e3-139">**Windows Server 2008 R2:** Essa propriedade não está disponível antes do Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f80e3-139">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="f80e3-140">**SBDbSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="f80e3-140">**SBDbSecondaryConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f80e3-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f80e3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f80e3-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f80e3-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f80e3-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f80e3-143">Optional.</span></span> <span data-ttu-id="f80e3-144">Cadeia de conexão de banco de dados secundária usada pelo serviço de agente de sessão para dar suporte à expiração da senha.</span><span class="sxs-lookup"><span data-stu-id="f80e3-144">Secondary database connection string, used by Session Broker service to support password expiration.</span></span>

<span data-ttu-id="f80e3-145">**Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Essa propriedade não está disponível antes do Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f80e3-145">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This property is not available prior to Windows Server 2016</span></span>

</dd> <dt>

<span data-ttu-id="f80e3-146">**SBNetworkName**</span><span class="sxs-lookup"><span data-stu-id="f80e3-146">**SBNetworkName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f80e3-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f80e3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f80e3-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f80e3-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f80e3-149">O nome de rede usado pelo serviço de agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="f80e3-149">The network name used by the session broker service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f80e3-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f80e3-150">Requirements</span></span>



| <span data-ttu-id="f80e3-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="f80e3-151">Requirement</span></span> | <span data-ttu-id="f80e3-152">Valor</span><span class="sxs-lookup"><span data-stu-id="f80e3-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f80e3-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f80e3-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f80e3-154">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f80e3-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f80e3-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f80e3-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f80e3-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f80e3-156">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="f80e3-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="f80e3-157">Namespace</span></span><br/>                | <span data-ttu-id="f80e3-158">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f80e3-158">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="f80e3-159">MOF</span><span class="sxs-lookup"><span data-stu-id="f80e3-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f80e3-160"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f80e3-160"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f80e3-161">DLL</span><span class="sxs-lookup"><span data-stu-id="f80e3-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f80e3-162"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f80e3-162"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

