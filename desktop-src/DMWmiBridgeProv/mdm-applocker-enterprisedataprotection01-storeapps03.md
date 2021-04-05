---
title: Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
description: A \_ classe MDM AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03 captura a lista de aplicativos do Windows que têm permissão para lidar com dados corporativos. Deve ser usado em conjunto com as configurações em./Vendor/MSFT/Policy/ConfigSource/DataProtection.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240f641e542bbbe0c71fd686e2d9df3908b9bab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919126"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a><span data-ttu-id="c13b5-106">\_Classe StoreApps03 do MDM AppLocker \_ EnterpriseDataProtection01 \_</span><span class="sxs-lookup"><span data-stu-id="c13b5-106">MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03 class</span></span>

<span data-ttu-id="c13b5-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c13b5-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c13b5-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c13b5-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c13b5-109">A classe **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** captura a lista de aplicativos do Windows que têm permissão para lidar com dados corporativos.</span><span class="sxs-lookup"><span data-stu-id="c13b5-109">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class captures the list of Windows apps that are allowed to handle enterprise data.</span></span> <span data-ttu-id="c13b5-110">Deve ser usado em conjunto com as configurações em./Vendor/MSFT/Policy/ConfigSource/DataProtection.</span><span class="sxs-lookup"><span data-stu-id="c13b5-110">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="c13b5-111">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c13b5-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c13b5-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c13b5-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="c13b5-113">Membros</span><span class="sxs-lookup"><span data-stu-id="c13b5-113">Members</span></span>

<span data-ttu-id="c13b5-114">A classe **StoreApps03 do MDM \_ AppLocker \_ EnterpriseDataProtection01 \_** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c13b5-114">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="c13b5-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c13b5-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c13b5-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c13b5-116">Properties</span></span>

<span data-ttu-id="c13b5-117">A classe **StoreApps03 do MDM \_ AppLocker \_ EnterpriseDataProtection01 \_** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c13b5-117">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c13b5-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c13b5-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13b5-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c13b5-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c13b5-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c13b5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c13b5-121">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c13b5-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c13b5-122">Define as restrições para a execução de aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="c13b5-122">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="c13b5-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c13b5-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13b5-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c13b5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c13b5-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c13b5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c13b5-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c13b5-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c13b5-127">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="c13b5-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="c13b5-128">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*GROUPING*"</span><span class="sxs-lookup"><span data-stu-id="c13b5-128">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="c13b5-129">**Política**</span><span class="sxs-lookup"><span data-stu-id="c13b5-129">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13b5-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c13b5-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c13b5-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c13b5-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c13b5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c13b5-132">Requirements</span></span>



| <span data-ttu-id="c13b5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c13b5-133">Requirement</span></span> | <span data-ttu-id="c13b5-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c13b5-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c13b5-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c13b5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c13b5-136">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c13b5-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c13b5-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c13b5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c13b5-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c13b5-138">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c13b5-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="c13b5-139">Namespace</span></span><br/>                | <span data-ttu-id="c13b5-140">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c13b5-140">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c13b5-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c13b5-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c13b5-142"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c13b5-142"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c13b5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c13b5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c13b5-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c13b5-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c13b5-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="c13b5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c13b5-146">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="c13b5-146">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

