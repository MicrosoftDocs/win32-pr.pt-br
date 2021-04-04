---
title: Classe MDM_DeviceStatus_UAC01
description: A \_ classe MDM DeviceStatus \_ UAC01 é usada pela empresa para consultar o status do UAC de dispositivos com suas políticas corporativas.
ms.assetid: fb1ca1bb-229e-4eaa-a1e3-e790c1dab760
keywords:
- Classe MDM_DeviceStatus_UAC01
- Classe MDM_DeviceStatus_UAC01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_UAC01
- MDM_DeviceStatus_UAC01.InstanceID
- MDM_DeviceStatus_UAC01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eecba42cd97bee660f66570e7f96c1ab2799f85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644929"
---
# <a name="mdm_devicestatus_uac01-class"></a><span data-ttu-id="61537-105">\_ \_ Classe UAC01 do MDM DeviceStatus</span><span class="sxs-lookup"><span data-stu-id="61537-105">MDM\_DeviceStatus\_UAC01 class</span></span>

<span data-ttu-id="61537-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="61537-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="61537-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="61537-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="61537-108">A classe **MDM \_ DeviceStatus \_ UAC01** é usada pela empresa para consultar o status do UAC de dispositivos com suas políticas corporativas.</span><span class="sxs-lookup"><span data-stu-id="61537-108">The **MDM\_DeviceStatus\_UAC01** class is used by the enterprise to query the UAC status of devices with their enterprise policies.</span></span>

<span data-ttu-id="61537-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="61537-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61537-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61537-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_UAC01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="61537-111">Membros</span><span class="sxs-lookup"><span data-stu-id="61537-111">Members</span></span>

<span data-ttu-id="61537-112">A **classe \_ \_ UAC01 de MDM DeviceStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="61537-112">The **MDM\_DeviceStatus\_UAC01** class has these types of members:</span></span>

-   [<span data-ttu-id="61537-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61537-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61537-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61537-114">Properties</span></span>

<span data-ttu-id="61537-115">A **classe \_ \_ UAC01 do MDM DeviceStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="61537-115">The **MDM\_DeviceStatus\_UAC01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61537-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="61537-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61537-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61537-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61537-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61537-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61537-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61537-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61537-120">Nó para a consulta UAC.</span><span class="sxs-lookup"><span data-stu-id="61537-120">Node for the UAC query.</span></span>

</dd> <dt>

<span data-ttu-id="61537-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="61537-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61537-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61537-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61537-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61537-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61537-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61537-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61537-125">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="61537-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="61537-126">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="61537-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="61537-127">Status</span><span class="sxs-lookup"><span data-stu-id="61537-127">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="61537-128">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="61537-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="61537-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61537-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61537-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61537-130">Requirements</span></span>



| <span data-ttu-id="61537-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="61537-131">Requirement</span></span> | <span data-ttu-id="61537-132">Valor</span><span class="sxs-lookup"><span data-stu-id="61537-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61537-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61537-133">Minimum supported client</span></span><br/> | <span data-ttu-id="61537-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="61537-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61537-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61537-135">Minimum supported server</span></span><br/> | <span data-ttu-id="61537-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61537-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="61537-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="61537-137">Namespace</span></span><br/>                | <span data-ttu-id="61537-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="61537-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="61537-139">MOF</span><span class="sxs-lookup"><span data-stu-id="61537-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61537-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61537-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="61537-141">DLL</span><span class="sxs-lookup"><span data-stu-id="61537-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61537-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61537-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

