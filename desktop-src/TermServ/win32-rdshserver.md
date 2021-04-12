---
title: Classe Win32_RDSHServer
description: Gerencia um servidor de Host da Sessão da Área de Trabalho Remota (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDSHServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDSHServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295792"
---
# <a name="win32_rdshserver-class"></a><span data-ttu-id="8a1eb-105">\_Classe Win32 RDSHServer</span><span class="sxs-lookup"><span data-stu-id="8a1eb-105">Win32\_RDSHServer class</span></span>

<span data-ttu-id="8a1eb-106">Gerencia um servidor de Host da Sessão da Área de Trabalho Remota (RDSH).</span><span class="sxs-lookup"><span data-stu-id="8a1eb-106">Manages a Remote Desktop Session Host (RDSH) server.</span></span>

<span data-ttu-id="8a1eb-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a1eb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a1eb-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a><span data-ttu-id="8a1eb-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8a1eb-109">Members</span></span>

<span data-ttu-id="8a1eb-110">A classe **Win32 \_ RDSHServer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8a1eb-110">The **Win32\_RDSHServer** class has these types of members:</span></span>

-   [<span data-ttu-id="8a1eb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a1eb-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8a1eb-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8a1eb-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8a1eb-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a1eb-113">Methods</span></span>

<span data-ttu-id="8a1eb-114">A classe **Win32 \_ RDSHServer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-114">The **Win32\_RDSHServer** class has these methods.</span></span>



| <span data-ttu-id="8a1eb-115">Método</span><span class="sxs-lookup"><span data-stu-id="8a1eb-115">Method</span></span>                                                                          | <span data-ttu-id="8a1eb-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a1eb-116">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a1eb-117">**Getint32property**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-117">**GetInt32Property**</span></span>](getint32property-win32-rdshserver.md)                   | <span data-ttu-id="8a1eb-118">Recupera um valor da propriedade Integer de um objeto **\_ RDSHServer do Win32** .</span><span class="sxs-lookup"><span data-stu-id="8a1eb-118">Retrieves an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="8a1eb-119">**GetPendingStartServerList**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-119">**GetPendingStartServerList**</span></span>](win32-rdshserver-getpendingstartserverlist.md) | <span data-ttu-id="8a1eb-120">Recupera uma lista de servidores que estão aguardando para serem iniciados.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-120">Retrieves a list of server waiting to start.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="8a1eb-121">**Getstringproperty**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-121">**GetStringProperty**</span></span>](getstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="8a1eb-122">Recupera um valor de propriedade da cadeia de caracteres de um objeto **\_ RDSHServer do Win32** .</span><span class="sxs-lookup"><span data-stu-id="8a1eb-122">Retrieves a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="8a1eb-123">**Setint32property**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-123">**SetInt32Property**</span></span>](setint32property-win32-rdshserver.md)                   | <span data-ttu-id="8a1eb-124">Atualiza um valor da propriedade Integer de um objeto **\_ RDSHServer do Win32** .</span><span class="sxs-lookup"><span data-stu-id="8a1eb-124">Updates an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="8a1eb-125">**Setstringproperty**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-125">**SetStringProperty**</span></span>](setstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="8a1eb-126">Atualiza um valor de propriedade de cadeia de caracteres de um objeto **Win32 \_ RDSHServer** .</span><span class="sxs-lookup"><span data-stu-id="8a1eb-126">Updates a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="8a1eb-127">**TestAndSetState**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-127">**TestAndSetState**</span></span>](win32-rdshserver-testandsetstate.md)                     | <span data-ttu-id="8a1eb-128">Compara o estado atual com o termo especificado; Se as duas corresponderem, o estado será definido como um novo valor.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-128">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="8a1eb-129">Independentemente da correspondência, o estado atual também é retornado.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-129">Regardless of the match, the current state is also returned.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8a1eb-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8a1eb-130">Properties</span></span>

<span data-ttu-id="8a1eb-131">A classe **Win32 \_ RDSHServer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-131">The **Win32\_RDSHServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a1eb-132">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-132">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a1eb-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a1eb-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a1eb-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8a1eb-135">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8a1eb-135">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8a1eb-136">Obtém e define o alias para a coleção de RDSH à qual o servidor de RDSH está atribuído.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-136">Gets and sets the alias to the RDSH collection to which the RDSH server is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="8a1eb-137">**ConnectionBroker**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-137">**ConnectionBroker**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a1eb-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a1eb-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a1eb-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a1eb-140">Obtém e define o nome do RDCB (agente de Conexão de Área de Trabalho Remota) que gerencia o acesso do usuário ao servidor de RDSH.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-140">Gets and sets the name of the Remote Desktop Connection Broker (RDCB) that manages user access to the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="8a1eb-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a1eb-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a1eb-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a1eb-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8a1eb-144">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8a1eb-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8a1eb-145">Obtém e define o nome do servidor de RDSH.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-145">Gets and sets the name of the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="8a1eb-146">**ServerState**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-146">**ServerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a1eb-147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a1eb-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a1eb-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a1eb-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a1eb-149">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8a1eb-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8a1eb-150">Descreve o estado do servidor.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-150">Describes the state of the server.</span></span> <span data-ttu-id="8a1eb-151">Qualquer valor diferente de **destino \_ em execução** (3) é reservado e deve considerar um estado inválido.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-151">Any value other than **TARGET\_RUNNING** (3) is reserved and should be consider an invalid state.</span></span>

<span data-ttu-id="8a1eb-152">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-152">The possible values are.</span></span>

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

<span data-ttu-id="8a1eb-153">**Destino \_ DESCONHECIDO** (1)</span><span class="sxs-lookup"><span data-stu-id="8a1eb-153">**TARGET\_UNKNOWN** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

<span data-ttu-id="8a1eb-154">**Destino \_ EM execução** (3)</span><span class="sxs-lookup"><span data-stu-id="8a1eb-154">**TARGET\_RUNNING** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

<span data-ttu-id="8a1eb-155">**Destino \_ INVÁLIDO** (8)</span><span class="sxs-lookup"><span data-stu-id="8a1eb-155">**TARGET\_INVALID** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

<span data-ttu-id="8a1eb-156">**Destino \_ A partir** de (9)</span><span class="sxs-lookup"><span data-stu-id="8a1eb-156">**TARGET\_STARTING** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

<span data-ttu-id="8a1eb-157">**Destino \_ PARAndo** (10)</span><span class="sxs-lookup"><span data-stu-id="8a1eb-157">**TARGET\_STOPPING** (10)</span></span>


<span data-ttu-id="8a1eb-158"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8a1eb-158"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="8a1eb-159">**Windows server 2012 R2 e Windows server 2012:** Essa propriedade não está disponível antes do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8a1eb-159">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a1eb-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a1eb-160">Requirements</span></span>



| <span data-ttu-id="8a1eb-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a1eb-161">Requirement</span></span> | <span data-ttu-id="8a1eb-162">Valor</span><span class="sxs-lookup"><span data-stu-id="8a1eb-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1eb-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a1eb-163">Minimum supported client</span></span><br/> | <span data-ttu-id="8a1eb-164">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8a1eb-164">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8a1eb-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a1eb-165">Minimum supported server</span></span><br/> | <span data-ttu-id="8a1eb-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a1eb-166">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8a1eb-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a1eb-167">Namespace</span></span><br/>                | <span data-ttu-id="8a1eb-168">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="8a1eb-168">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8a1eb-169">MOF</span><span class="sxs-lookup"><span data-stu-id="8a1eb-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a1eb-170"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a1eb-170"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a1eb-171">DLL</span><span class="sxs-lookup"><span data-stu-id="8a1eb-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a1eb-172"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a1eb-172"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8a1eb-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a1eb-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1eb-174">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="8a1eb-174">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

