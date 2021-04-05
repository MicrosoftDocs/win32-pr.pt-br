---
title: Classe MDM_DeviceStatus_CellularIdentities01_01
description: A \_ classe MDM DeviceStatus \_ CellularIdentities01 \_ 01 permite consultar se o dispositivo está em conformidade com a política de criptografia corporativa.
ms.assetid: e117ff72-48c0-4b25-8b09-c096851c18ac
keywords:
- Classe MDM_DeviceStatus_CellularIdentities01_01
- Classe MDM_DeviceStatus_CellularIdentities01_01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_CellularIdentities01_01
- MDM_DeviceStatus_CellularIdentities01_01.InstanceID
- MDM_DeviceStatus_CellularIdentities01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d9d3fab514fbfb56d132fc20ba98ef8c2565eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824604"
---
# <a name="mdm_devicestatus_cellularidentities01_01-class"></a><span data-ttu-id="fcd9a-105">\_Classe MDM DeviceStatus \_ CellularIdentities01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="fcd9a-105">MDM\_DeviceStatus\_CellularIdentities01\_01 class</span></span>

<span data-ttu-id="fcd9a-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fcd9a-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="fcd9a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fcd9a-108">A classe **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** permite consultar se o dispositivo está em conformidade com a política de criptografia corporativa.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-108">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="fcd9a-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd9a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcd9a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_CellularIdentities01_01
{
  string  InstanceID;
  string  ParentID;
  string  IMSI;
  string  ICCID;
  string  PhoneNumber;
  string  CommercializationOperator;
  boolean RoamingStatus;
  boolean RoamingCompliance;
};
```

## <a name="members"></a><span data-ttu-id="fcd9a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="fcd9a-111">Members</span></span>

<span data-ttu-id="fcd9a-112">A classe **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fcd9a-112">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="fcd9a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcd9a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcd9a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcd9a-114">Properties</span></span>

<span data-ttu-id="fcd9a-115">A classe **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-115">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fcd9a-116">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="fcd9a-116">CommercializationOperator</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd9a-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fcd9a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fcd9a-119">ICCID</span><span class="sxs-lookup"><span data-stu-id="fcd9a-119">ICCID</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd9a-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fcd9a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fcd9a-122">IMSI</span><span class="sxs-lookup"><span data-stu-id="fcd9a-122">IMSI</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-imsi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd9a-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fcd9a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fcd9a-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd9a-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcd9a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fcd9a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fcd9a-129">Nó para consultas em cartões SIM.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-129">Node for queries on SIM cards.</span></span>

</dd> <dt>

<span data-ttu-id="fcd9a-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd9a-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcd9a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fcd9a-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fcd9a-134">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="fcd9a-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="fcd9a-135">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="fcd9a-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="fcd9a-136">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="fcd9a-136">PhoneNumber</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-phonenumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd9a-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fcd9a-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fcd9a-139">RoamingCompliance</span><span class="sxs-lookup"><span data-stu-id="fcd9a-139">RoamingCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingcompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd9a-140">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fcd9a-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fcd9a-142">RoamingStatus</span><span class="sxs-lookup"><span data-stu-id="fcd9a-142">RoamingStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd9a-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fcd9a-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcd9a-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fcd9a-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcd9a-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcd9a-145">Requirements</span></span>



| <span data-ttu-id="fcd9a-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcd9a-146">Requirement</span></span> | <span data-ttu-id="fcd9a-147">Valor</span><span class="sxs-lookup"><span data-stu-id="fcd9a-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd9a-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcd9a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd9a-149">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fcd9a-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fcd9a-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcd9a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd9a-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fcd9a-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fcd9a-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="fcd9a-152">Namespace</span></span><br/>                | <span data-ttu-id="fcd9a-153">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="fcd9a-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fcd9a-154">MOF</span><span class="sxs-lookup"><span data-stu-id="fcd9a-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcd9a-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcd9a-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcd9a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="fcd9a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcd9a-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcd9a-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcd9a-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcd9a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd9a-159">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="fcd9a-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

