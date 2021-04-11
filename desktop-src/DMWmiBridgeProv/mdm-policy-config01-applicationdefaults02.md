---
title: Classe MDM_Policy_Config01_ApplicationDefaults02
description: A \_ classe MDM Policy \_ Config01 \_ ApplicationDefaults02 permite que um administrador defina o tipo de arquivo e as associações de protocolo padrão. Quando definido, as associações padrão serão aplicadas ao entrar no computador.
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- Classe MDM_Policy_Config01_ApplicationDefaults02
- Classe MDM_Policy_Config01_ApplicationDefaults02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246278b1e4185337ebb63d9d23f74e2ff8753615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454919"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a><span data-ttu-id="f1982-106">\_Classe MDM \_ Config01 \_ ApplicationDefaults02</span><span class="sxs-lookup"><span data-stu-id="f1982-106">MDM\_Policy\_Config01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="f1982-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f1982-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f1982-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f1982-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f1982-109">A \_ classe MDM Policy \_ Config01 \_ ApplicationDefaults02 permite que um administrador defina o tipo de arquivo e as associações de protocolo padrão.</span><span class="sxs-lookup"><span data-stu-id="f1982-109">The MDM\_Policy\_Config01\_ApplicationDefaults02 class allows an administrator to set default file type and protocol associations.</span></span> <span data-ttu-id="f1982-110">Quando definido, as associações padrão serão aplicadas ao entrar no computador.</span><span class="sxs-lookup"><span data-stu-id="f1982-110">When set, default associations will be applied on sign-in to the PC.</span></span>

<span data-ttu-id="f1982-111">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f1982-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1982-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1982-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="f1982-113">Membros</span><span class="sxs-lookup"><span data-stu-id="f1982-113">Members</span></span>

<span data-ttu-id="f1982-114">A **classe \_ \_ Config01 \_ ApplicationDefaults02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f1982-114">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="f1982-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1982-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1982-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1982-116">Properties</span></span>

<span data-ttu-id="f1982-117">A **classe \_ \_ Config01 \_ ApplicationDefaults02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1982-117">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f1982-118">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1982-118">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1982-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f1982-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1982-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f1982-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1982-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f1982-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1982-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f1982-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1982-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1982-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1982-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1982-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1982-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f1982-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1982-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f1982-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1982-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1982-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1982-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1982-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1982-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1982-129">Requirements</span></span>



| <span data-ttu-id="f1982-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1982-130">Requirement</span></span> | <span data-ttu-id="f1982-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f1982-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1982-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1982-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f1982-133">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f1982-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1982-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1982-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f1982-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f1982-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f1982-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1982-136">Namespace</span></span><br/>                | <span data-ttu-id="f1982-137">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f1982-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f1982-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f1982-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1982-139"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1982-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1982-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f1982-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1982-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1982-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

