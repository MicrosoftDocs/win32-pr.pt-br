---
title: Classe MDM_DeviceStatus_DeviceGuard01
description: A \_ classe MDM DeviceStatus \_ DeviceGuard01 é usada pela empresa para controlar o inventário de dispositivos e consultar o estado de conformidade desses dispositivos com suas políticas corporativas.
ms.assetid: 267129f6-ec37-43ae-bba3-e21917012f27
keywords:
- Classe MDM_DeviceStatus_DeviceGuard01
- Classe MDM_DeviceStatus_DeviceGuard01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_DeviceGuard01
- MDM_DeviceStatus_DeviceGuard01.InstanceID
- MDM_DeviceStatus_DeviceGuard01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5f4dffa67ad86b5486dce372018efd29e62620
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918849"
---
# <a name="mdm_devicestatus_deviceguard01-class"></a><span data-ttu-id="a6369-105">\_ \_ Classe DEVICEGUARD01 do MDM DeviceStatus</span><span class="sxs-lookup"><span data-stu-id="a6369-105">MDM\_DeviceStatus\_DeviceGuard01 class</span></span>

<span data-ttu-id="a6369-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="a6369-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a6369-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="a6369-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a6369-108">A \_ classe MDM DeviceStatus \_ DeviceGuard01 é usada pela empresa para controlar o inventário de dispositivos e consultar o estado de conformidade desses dispositivos com suas políticas corporativas.</span><span class="sxs-lookup"><span data-stu-id="a6369-108">The MDM\_DeviceStatus\_DeviceGuard01 class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="a6369-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a6369-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6369-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6369-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_DeviceGuard01
{
  string InstanceID;
  string ParentID;
  sint32 VirtualizationBasedSecurityHwReq;
  sint32 VirtualizationBasedSecurityStatus;
  sint32 LsaCfgCredGuardStatus;
};
```

## <a name="members"></a><span data-ttu-id="a6369-111">Membros</span><span class="sxs-lookup"><span data-stu-id="a6369-111">Members</span></span>

<span data-ttu-id="a6369-112">A **classe \_ \_ DeviceGuard01 de MDM DeviceStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a6369-112">The **MDM\_DeviceStatus\_DeviceGuard01** class has these types of members:</span></span>

-   [<span data-ttu-id="a6369-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a6369-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6369-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a6369-114">Properties</span></span>

<span data-ttu-id="a6369-115">A **classe \_ \_ DeviceGuard01 do MDM DeviceStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a6369-115">The **MDM\_DeviceStatus\_DeviceGuard01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6369-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a6369-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6369-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a6369-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6369-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a6369-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6369-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a6369-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a6369-120">LsaCfgCredGuardStatus</span><span class="sxs-lookup"><span data-stu-id="a6369-120">LsaCfgCredGuardStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-lsacfgcredguardstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6369-121">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a6369-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6369-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a6369-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a6369-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a6369-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6369-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a6369-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6369-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a6369-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6369-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a6369-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a6369-127">VirtualizationBasedSecurityHwReq</span><span class="sxs-lookup"><span data-stu-id="a6369-127">VirtualizationBasedSecurityHwReq</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecurityhwreq)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6369-128">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a6369-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6369-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a6369-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a6369-130">VirtualizationBasedSecurityStatus</span><span class="sxs-lookup"><span data-stu-id="a6369-130">VirtualizationBasedSecurityStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecuritystatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6369-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a6369-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6369-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a6369-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6369-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6369-133">Requirements</span></span>



| <span data-ttu-id="a6369-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6369-134">Requirement</span></span> | <span data-ttu-id="a6369-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a6369-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6369-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6369-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a6369-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a6369-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6369-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6369-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a6369-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a6369-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a6369-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6369-140">Namespace</span></span><br/>                | <span data-ttu-id="a6369-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="a6369-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a6369-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a6369-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6369-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6369-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6369-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a6369-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6369-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6369-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

