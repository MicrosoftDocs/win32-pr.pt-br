---
title: Classe MDM_DeviceStatus_NetworkIdentifiers01_01
description: A \_ classe MDM DeviceStatus \_ NetworkIdentifiers01 \_ 01 permite consultar um dispositivo para as propriedades de rede.
ms.assetid: 2439010e-62fa-4482-b280-b9f98d1fbb7b
keywords:
- Classe MDM_DeviceStatus_NetworkIdentifiers01_01
- Classe MDM_DeviceStatus_NetworkIdentifiers01_01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_NetworkIdentifiers01_01
- MDM_DeviceStatus_NetworkIdentifiers01_01.InstanceID
- MDM_DeviceStatus_NetworkIdentifiers01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530c301894d957c9a9a2db374f35cf7c1bcb5063
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009595"
---
# <a name="mdm_devicestatus_networkidentifiers01_01-class"></a><span data-ttu-id="40e1e-105">\_Classe MDM DeviceStatus \_ NetworkIdentifiers01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="40e1e-105">MDM\_DeviceStatus\_NetworkIdentifiers01\_01 class</span></span>

<span data-ttu-id="40e1e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="40e1e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="40e1e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="40e1e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="40e1e-108">A classe **MDM \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01** permite consultar um dispositivo para as propriedades de rede.</span><span class="sxs-lookup"><span data-stu-id="40e1e-108">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class allows you to query a device for network properties.</span></span>

<span data-ttu-id="40e1e-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="40e1e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="40e1e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40e1e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_NetworkIdentifiers01_01
{
  string  InstanceID;
  string  ParentID;
  string  IPAddressV4;
  string  IPAddressV6;
  boolean IsConnected;
  sint32  Type;
};
```

## <a name="members"></a><span data-ttu-id="40e1e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="40e1e-111">Members</span></span>

<span data-ttu-id="40e1e-112">A classe **MDM \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="40e1e-112">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="40e1e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="40e1e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40e1e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="40e1e-114">Properties</span></span>

<span data-ttu-id="40e1e-115">A classe **MDM \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="40e1e-115">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40e1e-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="40e1e-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e1e-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40e1e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40e1e-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40e1e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40e1e-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40e1e-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="40e1e-120">Nó para consultas em Propriedades de dispositivo e de rede.</span><span class="sxs-lookup"><span data-stu-id="40e1e-120">Node for queries on network and device properties.</span></span>

</dd> <dt>

[<span data-ttu-id="40e1e-121">IPAddressV4</span><span class="sxs-lookup"><span data-stu-id="40e1e-121">IPAddressV4</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e1e-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40e1e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40e1e-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="40e1e-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40e1e-124">IPAddressV6</span><span class="sxs-lookup"><span data-stu-id="40e1e-124">IPAddressV6</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv6)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e1e-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40e1e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40e1e-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="40e1e-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40e1e-127">IsConnected</span><span class="sxs-lookup"><span data-stu-id="40e1e-127">IsConnected</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-isconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e1e-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="40e1e-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40e1e-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="40e1e-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40e1e-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="40e1e-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e1e-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40e1e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40e1e-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40e1e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40e1e-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40e1e-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="40e1e-134">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="40e1e-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="40e1e-135">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="40e1e-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="40e1e-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="40e1e-136">Type</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40e1e-137">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="40e1e-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40e1e-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="40e1e-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40e1e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40e1e-139">Requirements</span></span>



| <span data-ttu-id="40e1e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="40e1e-140">Requirement</span></span> | <span data-ttu-id="40e1e-141">Valor</span><span class="sxs-lookup"><span data-stu-id="40e1e-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40e1e-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40e1e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="40e1e-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="40e1e-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40e1e-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40e1e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="40e1e-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="40e1e-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="40e1e-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="40e1e-146">Namespace</span></span><br/>                | <span data-ttu-id="40e1e-147">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="40e1e-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="40e1e-148">MOF</span><span class="sxs-lookup"><span data-stu-id="40e1e-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40e1e-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40e1e-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="40e1e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="40e1e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40e1e-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40e1e-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40e1e-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="40e1e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e1e-153">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="40e1e-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

