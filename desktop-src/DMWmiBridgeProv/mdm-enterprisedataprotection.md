---
title: Classe MDM_EnterpriseDataProtection
description: A \_ classe MDM EnterpriseDataProtection é usada para determinar o status atual das configurações específicas de WIP (proteção de informações do Windows) (anteriormente conhecidas como proteção de dados empresariais).
ms.assetid: 2b97de12-76d1-4b74-a979-f0484807b840
keywords:
- Classe MDM_EnterpriseDataProtection
- Classe MDM_EnterpriseDataProtection, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection.InstanceID
- MDM_EnterpriseDataProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b4a3a1d9d491b6970ee95a081de8bb240d54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455595"
---
# <a name="mdm_enterprisedataprotection-class"></a><span data-ttu-id="285cc-105">\_Classe EnterpriseDataProtection do MDM</span><span class="sxs-lookup"><span data-stu-id="285cc-105">MDM\_EnterpriseDataProtection class</span></span>

<span data-ttu-id="285cc-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="285cc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="285cc-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="285cc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="285cc-108">A classe **MDM \_ EnterpriseDataProtection** é usada para determinar o status atual das configurações específicas de WIP (proteção de informações do Windows) (anteriormente conhecidas como proteção de dados empresariais).</span><span class="sxs-lookup"><span data-stu-id="285cc-108">The **MDM\_EnterpriseDataProtection** class is used to determine the current status of Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span>

<span data-ttu-id="285cc-109">Para obter mais informações sobre WIP, consulte [proteger seus dados corporativos usando a EDP (proteção de dados empresariais)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="285cc-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="285cc-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="285cc-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="285cc-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="285cc-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="285cc-112">Membros</span><span class="sxs-lookup"><span data-stu-id="285cc-112">Members</span></span>

<span data-ttu-id="285cc-113">A classe **MDM \_ EnterpriseDataProtection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="285cc-113">The **MDM\_EnterpriseDataProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="285cc-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="285cc-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="285cc-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="285cc-115">Properties</span></span>

<span data-ttu-id="285cc-116">A classe **MDM \_ EnterpriseDataProtection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="285cc-116">The **MDM\_EnterpriseDataProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="285cc-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="285cc-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="285cc-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="285cc-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="285cc-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="285cc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="285cc-120">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="285cc-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="285cc-121">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="285cc-121">Identifies the name of the parent node.</span></span> <span data-ttu-id="285cc-122">Para essa classe, a cadeia de caracteres é "EnterpriseDataProtection".</span><span class="sxs-lookup"><span data-stu-id="285cc-122">For this class, the string is "EnterpriseDataProtection".</span></span>

</dd> <dt>

<span data-ttu-id="285cc-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="285cc-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="285cc-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="285cc-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="285cc-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="285cc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="285cc-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="285cc-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="285cc-127">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="285cc-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="285cc-128">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="285cc-128">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="285cc-129">Status</span><span class="sxs-lookup"><span data-stu-id="285cc-129">Status</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="285cc-130">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="285cc-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="285cc-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="285cc-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="285cc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="285cc-132">Requirements</span></span>



| <span data-ttu-id="285cc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="285cc-133">Requirement</span></span> | <span data-ttu-id="285cc-134">Valor</span><span class="sxs-lookup"><span data-stu-id="285cc-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285cc-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="285cc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="285cc-136">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="285cc-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="285cc-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="285cc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="285cc-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="285cc-138">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="285cc-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="285cc-139">Namespace</span></span><br/>                | <span data-ttu-id="285cc-140">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="285cc-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="285cc-141">MOF</span><span class="sxs-lookup"><span data-stu-id="285cc-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="285cc-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="285cc-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="285cc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="285cc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="285cc-144"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="285cc-144"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

