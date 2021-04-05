---
title: Classe MDM_Policy_Config01_Games02
description: A \_ classe Config01 Games02 de política de MDM \_ \_ configura os serviços de jogos avançados.
ms.assetid: 567cf1b0-9795-44d5-a002-a1c03a5bf45f
keywords:
- Classe MDM_Policy_Config01_Games02
- Classe MDM_Policy_Config01_Games02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Games02
- MDM_Policy_Config01_Games02.InstanceID
- MDM_Policy_Config01_Games02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f1ea989133bfdbe9d63dbaacff899dd7464965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009674"
---
# <a name="mdm_policy_config01_games02-class"></a><span data-ttu-id="525ae-105">\_Classe MDM \_ Config01 \_ Games02</span><span class="sxs-lookup"><span data-stu-id="525ae-105">MDM\_Policy\_Config01\_Games02 class</span></span>

<span data-ttu-id="525ae-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="525ae-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="525ae-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="525ae-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="525ae-108">A \_ classe Config01 Games02 de política de MDM \_ \_ configura os serviços de jogos avançados.</span><span class="sxs-lookup"><span data-stu-id="525ae-108">The MDM\_Policy\_Config01\_Games02 class configures the advanced gaming services.</span></span>

<span data-ttu-id="525ae-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="525ae-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="525ae-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="525ae-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Games02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAdvancedGamingServices;
};
```

## <a name="members"></a><span data-ttu-id="525ae-111">Membros</span><span class="sxs-lookup"><span data-stu-id="525ae-111">Members</span></span>

<span data-ttu-id="525ae-112">A **classe \_ \_ Config01 \_ Games02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="525ae-112">The **MDM\_Policy\_Config01\_Games02** class has these types of members:</span></span>

-   [<span data-ttu-id="525ae-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="525ae-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="525ae-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="525ae-114">Properties</span></span>

<span data-ttu-id="525ae-115">A **classe \_ \_ Config01 \_ Games02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="525ae-115">The **MDM\_Policy\_Config01\_Games02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="525ae-116">AllowAdvancedGamingServices</span><span class="sxs-lookup"><span data-stu-id="525ae-116">AllowAdvancedGamingServices</span></span>](/windows/client-management/mdm/policy-csp-games#games-allowadvancedgamingservices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="525ae-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="525ae-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="525ae-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="525ae-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="525ae-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="525ae-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="525ae-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="525ae-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="525ae-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="525ae-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="525ae-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="525ae-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="525ae-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="525ae-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="525ae-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="525ae-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="525ae-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="525ae-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="525ae-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="525ae-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="525ae-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="525ae-127">Requirements</span></span>



| <span data-ttu-id="525ae-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="525ae-128">Requirement</span></span> | <span data-ttu-id="525ae-129">Valor</span><span class="sxs-lookup"><span data-stu-id="525ae-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="525ae-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="525ae-130">Minimum supported client</span></span><br/> | <span data-ttu-id="525ae-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="525ae-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="525ae-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="525ae-132">Minimum supported server</span></span><br/> | <span data-ttu-id="525ae-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="525ae-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="525ae-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="525ae-134">Namespace</span></span><br/>                | <span data-ttu-id="525ae-135">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="525ae-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="525ae-136">MOF</span><span class="sxs-lookup"><span data-stu-id="525ae-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="525ae-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="525ae-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="525ae-138">DLL</span><span class="sxs-lookup"><span data-stu-id="525ae-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="525ae-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="525ae-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

