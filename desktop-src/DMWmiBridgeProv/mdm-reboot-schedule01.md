---
title: Classe MDM_Reboot_Schedule01
description: O \_ Schedule01class de reinicialização do MDM \_ é usado para configurar um horário específico para a reinicialização de um dispositivo.
ms.assetid: d865609a-9f17-4256-9c69-4fea75011c1f
keywords:
- Classe MDM_Reboot_Schedule01
- Classe MDM_Reboot_Schedule01, descrita
topic_type:
- apiref
api_name:
- MDM_Reboot_Schedule01
- MDM_Reboot_Schedule01.InstanceID
- MDM_Reboot_Schedule01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7229aca469ee83d9ac2e4b29f6d6b7c54875120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454671"
---
# <a name="mdm_reboot_schedule01-class"></a><span data-ttu-id="61a30-105">\_Classe Schedule01 de reinicialização do MDM \_</span><span class="sxs-lookup"><span data-stu-id="61a30-105">MDM\_Reboot\_Schedule01 class</span></span>

<span data-ttu-id="61a30-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="61a30-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="61a30-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="61a30-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="61a30-108">A **classe \_ \_ Schedule01 de reinicialização do MDM** é usada para configurar um horário específico para a reinicialização de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61a30-108">The **MDM\_Reboot\_Schedule01** class is used to configure a specific time for the reboot of a device.</span></span>

<span data-ttu-id="61a30-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="61a30-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a30-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61a30-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot_Schedule01
{
  string InstanceID;
  string ParentID;
  string Single;
  string DailyRecurrent;
};
```

## <a name="members"></a><span data-ttu-id="61a30-111">Membros</span><span class="sxs-lookup"><span data-stu-id="61a30-111">Members</span></span>

<span data-ttu-id="61a30-112">A **classe \_ \_ Schedule01 de reinicialização do MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="61a30-112">The **MDM\_Reboot\_Schedule01** class has these types of members:</span></span>

-   [<span data-ttu-id="61a30-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61a30-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61a30-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61a30-114">Properties</span></span>

<span data-ttu-id="61a30-115">A **classe \_ \_ Schedule01 de reinicialização do MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="61a30-115">The **MDM\_Reboot\_Schedule01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="61a30-116">DailyRecurrent</span><span class="sxs-lookup"><span data-stu-id="61a30-116">DailyRecurrent</span></span>](/windows/client-management/mdm/reboot-csp#schedule-dailyrecurrent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a30-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61a30-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a30-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61a30-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="61a30-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="61a30-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a30-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61a30-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a30-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61a30-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a30-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61a30-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61a30-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="61a30-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="61a30-124">Para essa classe, a cadeia de caracteres é "Schedule".</span><span class="sxs-lookup"><span data-stu-id="61a30-124">For this class, the string is "Schedule".</span></span>

</dd> <dt>

<span data-ttu-id="61a30-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="61a30-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a30-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61a30-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a30-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61a30-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a30-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61a30-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61a30-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="61a30-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="61a30-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Reboot"</span><span class="sxs-lookup"><span data-stu-id="61a30-130">For this class, the string is "./Vendor/MSFT/Reboot"</span></span>

</dd> <dt>

[<span data-ttu-id="61a30-131">Single</span><span class="sxs-lookup"><span data-stu-id="61a30-131">Single</span></span>](/windows/client-management/mdm/reboot-csp#schedule-single)
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a30-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61a30-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a30-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61a30-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61a30-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61a30-134">Requirements</span></span>



| <span data-ttu-id="61a30-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a30-135">Requirement</span></span> | <span data-ttu-id="61a30-136">Valor</span><span class="sxs-lookup"><span data-stu-id="61a30-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a30-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61a30-137">Minimum supported client</span></span><br/> | <span data-ttu-id="61a30-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="61a30-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="61a30-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61a30-139">Minimum supported server</span></span><br/> | <span data-ttu-id="61a30-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61a30-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="61a30-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="61a30-141">Namespace</span></span><br/>                | <span data-ttu-id="61a30-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="61a30-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="61a30-143">MOF</span><span class="sxs-lookup"><span data-stu-id="61a30-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61a30-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61a30-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="61a30-145">DLL</span><span class="sxs-lookup"><span data-stu-id="61a30-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61a30-146"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="61a30-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

