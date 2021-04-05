---
title: Classe MDM_Policy_Result01_ApplicationDefaults02
description: A \_ classe MDM Policy \_ Result01 \_ ApplicationDefaults02 representa as políticas de padrões de aplicativo disponíveis.
ms.assetid: bf7df9a1-7af1-49a6-9456-3e6ec48234e2
keywords:
- Classe MDM_Policy_Result01_ApplicationDefaults02
- Classe MDM_Policy_Result01_ApplicationDefaults02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationDefaults02
- MDM_Policy_Result01_ApplicationDefaults02.InstanceID
- MDM_Policy_Result01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10592ceb4e4f401ce9f64c24ef207a4e2e033e9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085624"
---
# <a name="mdm_policy_result01_applicationdefaults02-class"></a><span data-ttu-id="98e76-105">\_Classe MDM \_ Result01 \_ ApplicationDefaults02</span><span class="sxs-lookup"><span data-stu-id="98e76-105">MDM\_Policy\_Result01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="98e76-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="98e76-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="98e76-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="98e76-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="98e76-108">A \_ classe MDM Policy \_ Result01 \_ ApplicationDefaults02 representa as políticas de padrões de aplicativo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="98e76-108">The MDM\_Policy\_Result01\_ApplicationDefaults02 class represents the available application defaults policies.</span></span>

<span data-ttu-id="98e76-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="98e76-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e76-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98e76-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="98e76-111">Membros</span><span class="sxs-lookup"><span data-stu-id="98e76-111">Members</span></span>

<span data-ttu-id="98e76-112">A **classe \_ \_ Result01 \_ ApplicationDefaults02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="98e76-112">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="98e76-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="98e76-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98e76-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="98e76-114">Properties</span></span>

<span data-ttu-id="98e76-115">A **classe \_ \_ Result01 \_ ApplicationDefaults02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="98e76-115">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="98e76-116">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="98e76-116">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e76-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="98e76-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e76-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="98e76-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="98e76-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="98e76-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e76-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="98e76-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e76-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="98e76-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e76-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="98e76-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="98e76-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="98e76-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e76-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="98e76-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e76-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="98e76-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e76-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="98e76-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98e76-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98e76-127">Requirements</span></span>



| <span data-ttu-id="98e76-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="98e76-128">Requirement</span></span> | <span data-ttu-id="98e76-129">Valor</span><span class="sxs-lookup"><span data-stu-id="98e76-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e76-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98e76-130">Minimum supported client</span></span><br/> | <span data-ttu-id="98e76-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="98e76-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98e76-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98e76-132">Minimum supported server</span></span><br/> | <span data-ttu-id="98e76-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="98e76-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="98e76-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="98e76-134">Namespace</span></span><br/>                | <span data-ttu-id="98e76-135">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="98e76-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="98e76-136">MOF</span><span class="sxs-lookup"><span data-stu-id="98e76-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98e76-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98e76-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="98e76-138">DLL</span><span class="sxs-lookup"><span data-stu-id="98e76-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98e76-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98e76-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

