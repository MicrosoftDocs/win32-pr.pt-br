---
title: Classe MDM_Firewall_App04
description: A \_ classe App04 do MDM firewall \_ é usada para definir as configurações do Windows Defender firewall.
ms.assetid: d7844d89-97d3-43b4-85af-c9464d475167
keywords:
- Classe MDM_Firewall_App04
- Classe MDM_Firewall_App04, descrita
topic_type:
- apiref
api_name:
- MDM_Firewall_App04
- MDM_Firewall_App04.InstanceID
- MDM_Firewall_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a8558fb2834ba9b0143d644cf4922aa9a710d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085391"
---
# <a name="mdm_firewall_app04-class"></a><span data-ttu-id="9bfe3-105">\_ \_ Classe APP04 do MDM firewall</span><span class="sxs-lookup"><span data-stu-id="9bfe3-105">MDM\_Firewall\_App04 class</span></span>

<span data-ttu-id="9bfe3-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="9bfe3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9bfe3-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="9bfe3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9bfe3-108">A \_ classe App04 do MDM firewall \_ é usada para definir as configurações do Windows Defender firewall.</span><span class="sxs-lookup"><span data-stu-id="9bfe3-108">The MDM\_Firewall\_App04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="9bfe3-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9bfe3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bfe3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bfe3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_App04
{
  string InstanceID;
  string ParentID;
  string PackageFamilyName;
  string FilePath;
  string Fqbn;
  string ServiceName;
};
```

## <a name="members"></a><span data-ttu-id="9bfe3-111">Membros</span><span class="sxs-lookup"><span data-stu-id="9bfe3-111">Members</span></span>

<span data-ttu-id="9bfe3-112">A **classe \_ \_ App04 do MDM firewall** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9bfe3-112">The **MDM\_Firewall\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="9bfe3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9bfe3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9bfe3-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9bfe3-114">Properties</span></span>

<span data-ttu-id="9bfe3-115">A **classe \_ \_ App04 do MDM firewall** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9bfe3-115">The **MDM\_Firewall\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9bfe3-116">FilePath</span><span class="sxs-lookup"><span data-stu-id="9bfe3-116">FilePath</span></span>](/windows/client-management/mdm/firewall-csp#filepath)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfe3-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bfe3-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9bfe3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bfe3-119">Fqbn</span><span class="sxs-lookup"><span data-stu-id="9bfe3-119">Fqbn</span></span>](/windows/client-management/mdm/firewall-csp#fqbn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfe3-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bfe3-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9bfe3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9bfe3-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfe3-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bfe3-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bfe3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bfe3-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bfe3-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bfe3-126">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="9bfe3-126">PackageFamilyName</span></span>](/windows/client-management/mdm/firewall-csp#packagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfe3-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bfe3-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9bfe3-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9bfe3-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfe3-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bfe3-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bfe3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bfe3-132">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bfe3-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bfe3-133">ServiceName</span><span class="sxs-lookup"><span data-stu-id="9bfe3-133">ServiceName</span></span>](/windows/client-management/mdm/firewall-csp#servicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfe3-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bfe3-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bfe3-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9bfe3-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bfe3-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bfe3-136">Requirements</span></span>



| <span data-ttu-id="9bfe3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bfe3-137">Requirement</span></span> | <span data-ttu-id="9bfe3-138">Valor</span><span class="sxs-lookup"><span data-stu-id="9bfe3-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bfe3-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bfe3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9bfe3-140">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9bfe3-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9bfe3-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bfe3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9bfe3-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9bfe3-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9bfe3-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="9bfe3-143">Namespace</span></span><br/>                | <span data-ttu-id="9bfe3-144">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9bfe3-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="9bfe3-145">MOF</span><span class="sxs-lookup"><span data-stu-id="9bfe3-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bfe3-146"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bfe3-146"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bfe3-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9bfe3-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bfe3-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bfe3-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

