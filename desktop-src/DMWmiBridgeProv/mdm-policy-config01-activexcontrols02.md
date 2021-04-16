---
title: Classe MDM_Policy_Config01_ActiveXControls02
description: Essa configuração de política determina quais sites de instalação do ActiveX os usuários padrão em sua organização podem usar para instalar controles ActiveX em seus computadores.
ms.assetid: 242888ae-f07a-40b7-9539-29fcca9cfc40
keywords:
- Classe MDM_Policy_Config01_ActiveXControls02
- Classe MDM_Policy_Config01_ActiveXControls02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ActiveXControls02
- MDM_Policy_Config01_ActiveXControls02.InstanceID
- MDM_Policy_Config01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 213edcea47bc0fd3379f753613c5b884963ca781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811135"
---
# <a name="mdm_policy_config01_activexcontrols02-class"></a><span data-ttu-id="e77f8-105">\_Classe MDM \_ Config01 \_ ActiveXControls02</span><span class="sxs-lookup"><span data-stu-id="e77f8-105">MDM\_Policy\_Config01\_ActiveXControls02 class</span></span>

<span data-ttu-id="e77f8-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="e77f8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e77f8-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="e77f8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e77f8-108">Essa configuração de política determina quais sites de instalação do ActiveX os usuários padrão em sua organização podem usar para instalar controles ActiveX em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="e77f8-108">This policy setting determines which ActiveX installation sites standard users in your organization can use to install ActiveX controls on their computers.</span></span> <span data-ttu-id="e77f8-109">Quando essa configuração é habilitada, o administrador pode criar uma lista de sites de instalação do ActiveX aprovados especificados pela URL do host.</span><span class="sxs-lookup"><span data-stu-id="e77f8-109">When this setting is enabled, the administrator can create a list of approved Activex Install sites specified by host URL.</span></span>

<span data-ttu-id="e77f8-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e77f8-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e77f8-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e77f8-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a><span data-ttu-id="e77f8-112">Membros</span><span class="sxs-lookup"><span data-stu-id="e77f8-112">Members</span></span>

<span data-ttu-id="e77f8-113">A **classe \_ \_ Config01 \_ ActiveXControls02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e77f8-113">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these types of members:</span></span>

-   [<span data-ttu-id="e77f8-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e77f8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e77f8-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e77f8-115">Properties</span></span>

<span data-ttu-id="e77f8-116">A **classe \_ \_ Config01 \_ ActiveXControls02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e77f8-116">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e77f8-117">ApprovedInstallationSites</span><span class="sxs-lookup"><span data-stu-id="e77f8-117">ApprovedInstallationSites</span></span>](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e77f8-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e77f8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e77f8-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e77f8-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e77f8-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e77f8-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e77f8-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e77f8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e77f8-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e77f8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e77f8-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e77f8-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e77f8-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e77f8-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e77f8-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e77f8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e77f8-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e77f8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e77f8-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e77f8-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e77f8-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e77f8-128">Requirements</span></span>



| <span data-ttu-id="e77f8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e77f8-129">Requirement</span></span> | <span data-ttu-id="e77f8-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e77f8-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e77f8-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e77f8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e77f8-132">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e77f8-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e77f8-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e77f8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e77f8-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e77f8-134">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e77f8-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="e77f8-135">Namespace</span></span><br/>                | <span data-ttu-id="e77f8-136">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="e77f8-136">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e77f8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e77f8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e77f8-138"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e77f8-138"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e77f8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e77f8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e77f8-140"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e77f8-140"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

