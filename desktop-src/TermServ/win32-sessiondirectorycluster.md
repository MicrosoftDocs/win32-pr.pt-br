---
title: Classe Win32_SessionDirectoryCluster
description: Fornece propriedades para exibir as propriedades de um farm no agente do Conexão de Área de Trabalho Remota (agente de conexão RD).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionDirectoryCluster Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionDirectoryCluster classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454975"
---
# <a name="win32_sessiondirectorycluster-class"></a><span data-ttu-id="44008-105">\_Classe Win32 SessionDirectoryCluster</span><span class="sxs-lookup"><span data-stu-id="44008-105">Win32\_SessionDirectoryCluster class</span></span>

<span data-ttu-id="44008-106">Fornece propriedades para exibir as propriedades de um farm no agente do Conexão de Área de Trabalho Remota (agente de conexão RD).</span><span class="sxs-lookup"><span data-stu-id="44008-106">Provides properties for viewing the properties of a farm in Remote Desktop Connection Broker (RD Connection Broker).</span></span>

> [!Note]  
> <span data-ttu-id="44008-107">No Windows Server 2008 R2, o nome do agente de sessão dos serviços de terminal (agente de Sessão TS) foi alterado para o agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="44008-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="44008-108">Essas propriedades se aplicam a todos os sistemas operacionais com suporte, salvo indicação em contrário.</span><span class="sxs-lookup"><span data-stu-id="44008-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="44008-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44008-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a><span data-ttu-id="44008-110">Membros</span><span class="sxs-lookup"><span data-stu-id="44008-110">Members</span></span>

<span data-ttu-id="44008-111">A classe **Win32 \_ SessionDirectoryCluster** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="44008-111">The **Win32\_SessionDirectoryCluster** class has these types of members:</span></span>

-   [<span data-ttu-id="44008-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="44008-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44008-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="44008-113">Properties</span></span>

<span data-ttu-id="44008-114">A classe **Win32 \_ SessionDirectoryCluster** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="44008-114">The **Win32\_SessionDirectoryCluster** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44008-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="44008-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44008-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44008-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44008-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44008-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44008-118">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44008-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44008-119">Nome do farm no agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="44008-119">Name of the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="44008-120">**NumberOfServers**</span><span class="sxs-lookup"><span data-stu-id="44008-120">**NumberOfServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44008-121">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44008-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44008-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44008-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44008-123">Número de servidores no farm no agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="44008-123">Number of servers in the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="44008-124">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="44008-124">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44008-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44008-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44008-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44008-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44008-127">Modo de sessão única do farm no agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="44008-127">Single session mode of the farm in RD Connection Broker.</span></span>

<dt>

<span data-ttu-id="44008-128">0</span><span class="sxs-lookup"><span data-stu-id="44008-128">0</span></span>
</dt> <dd>

<span data-ttu-id="44008-129">O farm no agente de conexão de área de trabalho remota não está no modo de sessão única.</span><span class="sxs-lookup"><span data-stu-id="44008-129">The farm in RD Connection Broker is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="44008-130">1</span><span class="sxs-lookup"><span data-stu-id="44008-130">1</span></span>
</dt> <dd>

<span data-ttu-id="44008-131">O farm no agente de conexão de área de trabalho remota está em modo de sessão única.</span><span class="sxs-lookup"><span data-stu-id="44008-131">The farm in RD Connection Broker is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44008-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="44008-132">Remarks</span></span>

<span data-ttu-id="44008-133">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="44008-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="44008-134">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="44008-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="44008-135">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="44008-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="44008-136">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="44008-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="44008-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44008-137">Requirements</span></span>



| <span data-ttu-id="44008-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="44008-138">Requirement</span></span> | <span data-ttu-id="44008-139">Valor</span><span class="sxs-lookup"><span data-stu-id="44008-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44008-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44008-140">Minimum supported client</span></span><br/> | <span data-ttu-id="44008-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="44008-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="44008-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44008-142">Minimum supported server</span></span><br/> | <span data-ttu-id="44008-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44008-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="44008-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="44008-144">Namespace</span></span><br/>                | <span data-ttu-id="44008-145">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="44008-145">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="44008-146">MOF</span><span class="sxs-lookup"><span data-stu-id="44008-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44008-147"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44008-147"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="44008-148">DLL</span><span class="sxs-lookup"><span data-stu-id="44008-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44008-149"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44008-149"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44008-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="44008-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44008-151">**\_SessionDirectoryServer Win32**</span><span class="sxs-lookup"><span data-stu-id="44008-151">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> <dt>

[<span data-ttu-id="44008-152">**\_SessionDirectorySession Win32**</span><span class="sxs-lookup"><span data-stu-id="44008-152">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

