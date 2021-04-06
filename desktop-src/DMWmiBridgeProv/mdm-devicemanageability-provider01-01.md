---
title: Classe MDM_DeviceManageability_Provider01_01
description: A \_ classe MDM DeviceManageability \_ Provider01 \_ 01 é usada para recuperar as informações gerais sobre os recursos de configuração do MDM no dispositivo.
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- Classe MDM_DeviceManageability_Provider01_01
- Classe MDM_DeviceManageability_Provider01_01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1ef064bcffd5303a3ef820dc0b463a3b5e622b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824606"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a><span data-ttu-id="7148c-105">\_Classe MDM DeviceManageability \_ Provider01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="7148c-105">MDM\_DeviceManageability\_Provider01\_01 class</span></span>

<span data-ttu-id="7148c-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7148c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7148c-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7148c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7148c-108">A \_ classe MDM DeviceManageability \_ Provider01 \_ 01 é usada para recuperar as informações gerais sobre os recursos de configuração do MDM no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7148c-108">The MDM\_DeviceManageability\_Provider01\_01 class is used retrieve the general information about MDM configuration capabilities on the device.</span></span>

<span data-ttu-id="7148c-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7148c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7148c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7148c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a><span data-ttu-id="7148c-111">Membros</span><span class="sxs-lookup"><span data-stu-id="7148c-111">Members</span></span>

<span data-ttu-id="7148c-112">A classe **MDM \_ DeviceManageability \_ Provider01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7148c-112">The **MDM\_DeviceManageability\_Provider01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="7148c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7148c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7148c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7148c-114">Properties</span></span>

<span data-ttu-id="7148c-115">A classe **MDM \_ DeviceManageability \_ Provider01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7148c-115">The **MDM\_DeviceManageability\_Provider01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7148c-116">ConfigInfo</span><span class="sxs-lookup"><span data-stu-id="7148c-116">ConfigInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7148c-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7148c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7148c-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7148c-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7148c-119">Você deve definir o valor para \_ servidor de ponte WMI \_ .</span><span class="sxs-lookup"><span data-stu-id="7148c-119">You must set the value to WMI\_Bridge\_Server.</span></span> <span data-ttu-id="7148c-120">O chamador não pode definir a ID do provedor dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="7148c-120">The caller cannot dynamically set the Provider ID.</span></span>

</dd> <dt>

[<span data-ttu-id="7148c-121">EnrollmentInfo</span><span class="sxs-lookup"><span data-stu-id="7148c-121">EnrollmentInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7148c-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7148c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7148c-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7148c-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7148c-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7148c-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7148c-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7148c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7148c-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7148c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7148c-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7148c-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7148c-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7148c-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7148c-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7148c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7148c-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7148c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7148c-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7148c-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7148c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7148c-132">Requirements</span></span>



| <span data-ttu-id="7148c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7148c-133">Requirement</span></span> | <span data-ttu-id="7148c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="7148c-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7148c-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7148c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7148c-136">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7148c-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7148c-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7148c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7148c-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7148c-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7148c-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="7148c-139">Namespace</span></span><br/>                | <span data-ttu-id="7148c-140">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7148c-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="7148c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7148c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7148c-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7148c-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="7148c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7148c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7148c-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7148c-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

