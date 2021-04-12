---
title: Classe Win32_SessionBrokerFarm
description: Define a consulta para um farm de agente de sessão.
ms.assetid: 55a2a7ea-e891-4723-b919-ee3c908eaffb
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionBrokerFarm Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionBrokerFarm classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarm
- Win32_SessionBrokerFarm.PluginName
- Win32_SessionBrokerFarm.FarmName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a3ccbb5e1e08a036fb9973d552db73ee1607c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455139"
---
# <a name="win32_sessionbrokerfarm-class"></a><span data-ttu-id="264d4-105">\_Classe Win32 SessionBrokerFarm</span><span class="sxs-lookup"><span data-stu-id="264d4-105">Win32\_SessionBrokerFarm class</span></span>

<span data-ttu-id="264d4-106">Define a consulta para um farm de agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="264d4-106">Defines the query for a session broker farm.</span></span>

<span data-ttu-id="264d4-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="264d4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="264d4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="264d4-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARM_Prov"), AMENDMENT]
class Win32_SessionBrokerFarm
{
  string PluginName;
  string FarmName;
};
```

## <a name="members"></a><span data-ttu-id="264d4-109">Membros</span><span class="sxs-lookup"><span data-stu-id="264d4-109">Members</span></span>

<span data-ttu-id="264d4-110">A classe **Win32 \_ SessionBrokerFarm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="264d4-110">The **Win32\_SessionBrokerFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="264d4-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="264d4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="264d4-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="264d4-112">Properties</span></span>

<span data-ttu-id="264d4-113">A classe **Win32 \_ SessionBrokerFarm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="264d4-113">The **Win32\_SessionBrokerFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="264d4-114">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="264d4-114">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264d4-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="264d4-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="264d4-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="264d4-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="264d4-117">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="264d4-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="264d4-118">O nome do farm de agente de sessão que precisa ser consultado.</span><span class="sxs-lookup"><span data-stu-id="264d4-118">The name of the session broker farm that needs to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="264d4-119">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="264d4-119">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="264d4-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="264d4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="264d4-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="264d4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="264d4-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="264d4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="264d4-123">O nome do plug-in.</span><span class="sxs-lookup"><span data-stu-id="264d4-123">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="264d4-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="264d4-124">Examples</span></span>

<span data-ttu-id="264d4-125">A cadeia de caracteres de consulta a seguir demonstra como a classe **\_ SessionBrokerFarm do Win32** é usada em uma consulta.</span><span class="sxs-lookup"><span data-stu-id="264d4-125">The following query string demonstrates how the **Win32\_SessionBrokerFarm** class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerFarm WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="264d4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="264d4-126">Requirements</span></span>



| <span data-ttu-id="264d4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="264d4-127">Requirement</span></span> | <span data-ttu-id="264d4-128">Valor</span><span class="sxs-lookup"><span data-stu-id="264d4-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="264d4-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="264d4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="264d4-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="264d4-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="264d4-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="264d4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="264d4-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="264d4-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="264d4-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="264d4-133">Namespace</span></span><br/>                | <span data-ttu-id="264d4-134">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="264d4-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="264d4-135">MOF</span><span class="sxs-lookup"><span data-stu-id="264d4-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="264d4-136"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="264d4-136"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="264d4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="264d4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="264d4-138"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="264d4-138"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

