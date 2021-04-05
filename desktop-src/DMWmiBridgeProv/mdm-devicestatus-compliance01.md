---
title: Classe MDM_DeviceStatus_Compliance01
description: A \_ classe MDM DeviceStatus \_ Compliance01 permite consultar se o dispositivo está em conformidade com a política de criptografia corporativa.
ms.assetid: 99c4cb9b-ae53-432c-b970-d61fb8496123
keywords:
- Classe MDM_DeviceStatus_Compliance01
- Classe MDM_DeviceStatus_Compliance01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01.InstanceID
- MDM_DeviceStatus_Compliance01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf606b7f10fbe7abc196622ee54b271e5285f2c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085998"
---
# <a name="mdm_devicestatus_compliance01-class"></a><span data-ttu-id="d9bb6-105">\_ \_ Classe COMPLIANCE01 do MDM DeviceStatus</span><span class="sxs-lookup"><span data-stu-id="d9bb6-105">MDM\_DeviceStatus\_Compliance01 class</span></span>

<span data-ttu-id="d9bb6-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d9bb6-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="d9bb6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d9bb6-108">A classe **MDM \_ DeviceStatus \_ Compliance01** permite consultar se o dispositivo está em conformidade com a política de criptografia corporativa.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-108">The **MDM\_DeviceStatus\_Compliance01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="d9bb6-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bb6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9bb6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Compliance01
{
  string  InstanceID;
  string  ParentID;
  boolean EncryptionCompliance;
};
```

## <a name="members"></a><span data-ttu-id="d9bb6-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d9bb6-111">Members</span></span>

<span data-ttu-id="d9bb6-112">A **classe \_ \_ Compliance01 de MDM DeviceStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d9bb6-112">The **MDM\_DeviceStatus\_Compliance01** class has these types of members:</span></span>

-   [<span data-ttu-id="d9bb6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9bb6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9bb6-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9bb6-114">Properties</span></span>

<span data-ttu-id="d9bb6-115">A **classe \_ \_ Compliance01 do MDM DeviceStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-115">The **MDM\_DeviceStatus\_Compliance01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d9bb6-116">EncryptionCompliance</span><span class="sxs-lookup"><span data-stu-id="d9bb6-116">EncryptionCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-compliance-encryptioncompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9bb6-117">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d9bb6-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9bb6-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9bb6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9bb6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d9bb6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9bb6-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9bb6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9bb6-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9bb6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9bb6-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9bb6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d9bb6-123">Nó para consultas sobre conformidade.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-123">Node for queries on compliance.</span></span>

</dd> <dt>

<span data-ttu-id="d9bb6-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d9bb6-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9bb6-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9bb6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9bb6-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9bb6-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9bb6-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9bb6-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d9bb6-128">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="d9bb6-129">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="d9bb6-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9bb6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9bb6-130">Requirements</span></span>



| <span data-ttu-id="d9bb6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9bb6-131">Requirement</span></span> | <span data-ttu-id="d9bb6-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d9bb6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bb6-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9bb6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d9bb6-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d9bb6-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9bb6-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9bb6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d9bb6-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d9bb6-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d9bb6-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9bb6-137">Namespace</span></span><br/>                | <span data-ttu-id="d9bb6-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d9bb6-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d9bb6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d9bb6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9bb6-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9bb6-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9bb6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d9bb6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9bb6-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9bb6-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9bb6-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9bb6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9bb6-144">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="d9bb6-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

