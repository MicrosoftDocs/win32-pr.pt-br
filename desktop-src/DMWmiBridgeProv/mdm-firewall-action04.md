---
title: Classe MDM_Firewall_Action04
description: A \_ classe Action04 do MDM firewall \_ é usada para definir as configurações do Windows Defender firewall.
ms.assetid: d0704662-ac2b-4ff5-a2c1-8f2bc7835488
keywords:
- Classe MDM_Firewall_Action04
- Classe MDM_Firewall_Action04, descrita
topic_type:
- apiref
api_name:
- MDM_Firewall_Action04
- MDM_Firewall_Action04.InstanceID
- MDM_Firewall_Action04.ParentID
- MDM_Firewall_Action04.Type
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1eede757f6a3e129300e6d81a28d34248dda1f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454925"
---
# <a name="mdm_firewall_action04-class"></a><span data-ttu-id="5ce4f-105">\_ \_ Classe ACTION04 do MDM firewall</span><span class="sxs-lookup"><span data-stu-id="5ce4f-105">MDM\_Firewall\_Action04 class</span></span>

<span data-ttu-id="5ce4f-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="5ce4f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5ce4f-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="5ce4f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5ce4f-108">A \_ classe Action04 do MDM firewall \_ é usada para definir as configurações do Windows Defender firewall.</span><span class="sxs-lookup"><span data-stu-id="5ce4f-108">The MDM\_Firewall\_Action04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="5ce4f-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5ce4f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce4f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ce4f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Action04
{
  string InstanceID;
  string ParentID;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="5ce4f-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5ce4f-111">Members</span></span>

<span data-ttu-id="5ce4f-112">A **classe \_ \_ Action04 do MDM firewall** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5ce4f-112">The **MDM\_Firewall\_Action04** class has these types of members:</span></span>

-   [<span data-ttu-id="5ce4f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ce4f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ce4f-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ce4f-114">Properties</span></span>

<span data-ttu-id="5ce4f-115">A **classe \_ \_ Action04 do MDM firewall** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5ce4f-115">The **MDM\_Firewall\_Action04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ce4f-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5ce4f-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce4f-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ce4f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ce4f-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ce4f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ce4f-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ce4f-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5ce4f-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5ce4f-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce4f-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ce4f-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ce4f-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ce4f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ce4f-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ce4f-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5ce4f-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5ce4f-124">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce4f-125">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ce4f-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ce4f-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5ce4f-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ce4f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ce4f-127">Requirements</span></span>



| <span data-ttu-id="5ce4f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ce4f-128">Requirement</span></span> | <span data-ttu-id="5ce4f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5ce4f-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce4f-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ce4f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5ce4f-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5ce4f-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ce4f-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ce4f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5ce4f-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5ce4f-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="5ce4f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ce4f-134">Namespace</span></span><br/>                | <span data-ttu-id="5ce4f-135">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5ce4f-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="5ce4f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5ce4f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ce4f-137"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ce4f-137"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ce4f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5ce4f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ce4f-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ce4f-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

