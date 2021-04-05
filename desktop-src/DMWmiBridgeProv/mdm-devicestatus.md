---
title: Classe MDM_DeviceStatus
description: A \_ classe MDM DeviceStatus é usada pela empresa para controlar o inventário de dispositivos e consultar o estado de conformidade desses dispositivos com suas políticas corporativas.
ms.assetid: fceaaf36-8f33-410a-89b4-c824b10164d5
keywords:
- Classe MDM_DeviceStatus
- Classe MDM_DeviceStatus, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus
- MDM_DeviceStatus.InstanceID
- MDM_DeviceStatus.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751a33553b4a00ac6719ce6e24c75a03444f0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085994"
---
# <a name="mdm_devicestatus-class"></a><span data-ttu-id="19141-105">\_Classe DeviceStatus do MDM</span><span class="sxs-lookup"><span data-stu-id="19141-105">MDM\_DeviceStatus class</span></span>

<span data-ttu-id="19141-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="19141-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="19141-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="19141-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="19141-108">A classe **MDM \_ DeviceStatus** é usada pela empresa para controlar o inventário de dispositivos e consultar o estado de conformidade desses dispositivos com suas políticas corporativas.</span><span class="sxs-lookup"><span data-stu-id="19141-108">The **MDM\_DeviceStatus** class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="19141-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="19141-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19141-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19141-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus
{
  string InstanceID;
  string ParentID;
  sint32 SecureBootState;
  string DomainName;
};
```

## <a name="members"></a><span data-ttu-id="19141-111">Membros</span><span class="sxs-lookup"><span data-stu-id="19141-111">Members</span></span>

<span data-ttu-id="19141-112">A classe **MDM \_ DeviceStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="19141-112">The **MDM\_DeviceStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="19141-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="19141-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19141-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="19141-114">Properties</span></span>

<span data-ttu-id="19141-115">A classe **MDM \_ DeviceStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="19141-115">The **MDM\_DeviceStatus** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="19141-116">DomainName</span><span class="sxs-lookup"><span data-stu-id="19141-116">DomainName</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19141-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19141-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19141-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19141-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19141-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="19141-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19141-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19141-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19141-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19141-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19141-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19141-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19141-123">O nó raiz do provedor de serviços de configuração do DeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="19141-123">The root node for the DeviceStatus configuration service provider.</span></span>

</dd> <dt>

<span data-ttu-id="19141-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="19141-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19141-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19141-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19141-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19141-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19141-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19141-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19141-128">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="19141-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="19141-129">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="19141-129">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="19141-130">SecureBootState</span><span class="sxs-lookup"><span data-stu-id="19141-130">SecureBootState</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-securebootstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19141-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="19141-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="19141-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19141-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19141-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19141-133">Requirements</span></span>



| <span data-ttu-id="19141-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="19141-134">Requirement</span></span> | <span data-ttu-id="19141-135">Valor</span><span class="sxs-lookup"><span data-stu-id="19141-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19141-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19141-136">Minimum supported client</span></span><br/> | <span data-ttu-id="19141-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="19141-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19141-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19141-138">Minimum supported server</span></span><br/> | <span data-ttu-id="19141-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="19141-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="19141-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="19141-140">Namespace</span></span><br/>                | <span data-ttu-id="19141-141">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="19141-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="19141-142">MOF</span><span class="sxs-lookup"><span data-stu-id="19141-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19141-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19141-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="19141-144">DLL</span><span class="sxs-lookup"><span data-stu-id="19141-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19141-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19141-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19141-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="19141-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19141-147">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="19141-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

