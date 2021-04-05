---
title: Classe MDM_Policy_Config01_Handwriting02
description: A \_ classe MDM Policy \_ Config01 \_ Handwriting02 é usada para configurar o modo padrão para o painel de manuscrito.
ms.assetid: 3b835b72-7985-45c9-afc4-b6fdc69b331b
keywords:
- Classe MDM_Policy_Config01_Handwriting02
- Classe MDM_Policy_Config01_Handwriting02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Handwriting02
- MDM_Policy_Config01_Handwriting02.InstanceID
- MDM_Policy_Config01_Handwriting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef2aa5f8b6563126dfcdd9e75870334853db11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824705"
---
# <a name="mdm_policy_config01_handwriting02-class"></a><span data-ttu-id="791e7-105">\_Classe MDM \_ Config01 \_ Handwriting02</span><span class="sxs-lookup"><span data-stu-id="791e7-105">MDM\_Policy\_Config01\_Handwriting02 class</span></span>

<span data-ttu-id="791e7-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="791e7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="791e7-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="791e7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="791e7-108">A \_ classe MDM Policy \_ Config01 \_ Handwriting02 é usada para configurar o modo padrão para o painel de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="791e7-108">The MDM\_Policy\_Config01\_Handwriting02 class is used to configure the default mode for the handwriting panel.</span></span>

<span data-ttu-id="791e7-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="791e7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="791e7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="791e7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Handwriting02
{
  string InstanceID;
  string ParentID;
  sint32 PanelDefaultModeDocked;
};
```

## <a name="members"></a><span data-ttu-id="791e7-111">Membros</span><span class="sxs-lookup"><span data-stu-id="791e7-111">Members</span></span>

<span data-ttu-id="791e7-112">A **classe \_ \_ Config01 \_ Handwriting02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="791e7-112">The **MDM\_Policy\_Config01\_Handwriting02** class has these types of members:</span></span>

-   [<span data-ttu-id="791e7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="791e7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="791e7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="791e7-114">Properties</span></span>

<span data-ttu-id="791e7-115">A **classe \_ \_ Config01 \_ Handwriting02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="791e7-115">The **MDM\_Policy\_Config01\_Handwriting02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="791e7-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="791e7-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="791e7-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="791e7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="791e7-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="791e7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="791e7-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="791e7-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="791e7-120">PanelDefaultModeDocked</span><span class="sxs-lookup"><span data-stu-id="791e7-120">PanelDefaultModeDocked</span></span>](/windows/client-management/mdm/policy-csp-handwriting#handwriting-paneldefaultmodedocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="791e7-121">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="791e7-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="791e7-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="791e7-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="791e7-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="791e7-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="791e7-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="791e7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="791e7-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="791e7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="791e7-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="791e7-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="791e7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="791e7-127">Requirements</span></span>



| <span data-ttu-id="791e7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="791e7-128">Requirement</span></span> | <span data-ttu-id="791e7-129">Valor</span><span class="sxs-lookup"><span data-stu-id="791e7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="791e7-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="791e7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="791e7-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="791e7-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="791e7-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="791e7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="791e7-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="791e7-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="791e7-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="791e7-134">Namespace</span></span><br/>                | <span data-ttu-id="791e7-135">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="791e7-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="791e7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="791e7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="791e7-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="791e7-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="791e7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="791e7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="791e7-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="791e7-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

