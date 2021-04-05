---
title: Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03
description: A \_ classe MDM AppLocker \_ EnterpriseDataProtection01 \_ EXE03 captura a lista de aplicativos executáveis que têm permissão para lidar com dados corporativos.
ms.assetid: 43f253d4-3f9d-4651-91b4-b7460706e8b4
keywords:
- Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03
- Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6cbaba46034c26524ca7e12aaa93b588708f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086379"
---
# <a name="mdm_applocker_enterprisedataprotection01_exe03-class"></a><span data-ttu-id="b2daf-105">\_Classe EXE03 do MDM AppLocker \_ EnterpriseDataProtection01 \_</span><span class="sxs-lookup"><span data-stu-id="b2daf-105">MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03 class</span></span>

<span data-ttu-id="b2daf-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b2daf-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b2daf-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b2daf-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b2daf-108">A classe **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** captura a lista de aplicativos executáveis que têm permissão para lidar com dados corporativos.</span><span class="sxs-lookup"><span data-stu-id="b2daf-108">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class captures the list of executable applications that are allowed to handle enterprise data.</span></span> <span data-ttu-id="b2daf-109">Deve ser usado em conjunto com as configurações em./Vendor/MSFT/Policy/ConfigSource/DataProtection.</span><span class="sxs-lookup"><span data-stu-id="b2daf-109">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="b2daf-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b2daf-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2daf-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2daf-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="b2daf-112">Membros</span><span class="sxs-lookup"><span data-stu-id="b2daf-112">Members</span></span>

<span data-ttu-id="b2daf-113">A classe **EXE03 do MDM \_ AppLocker \_ EnterpriseDataProtection01 \_** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b2daf-113">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="b2daf-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b2daf-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2daf-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b2daf-115">Properties</span></span>

<span data-ttu-id="b2daf-116">A classe **EXE03 do MDM \_ AppLocker \_ EnterpriseDataProtection01 \_** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b2daf-116">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2daf-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b2daf-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2daf-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b2daf-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2daf-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b2daf-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2daf-120">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2daf-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2daf-121">Define as restrições para iniciar aplicativos executáveis.</span><span class="sxs-lookup"><span data-stu-id="b2daf-121">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

<span data-ttu-id="b2daf-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b2daf-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2daf-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b2daf-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2daf-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b2daf-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2daf-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2daf-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2daf-126">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="b2daf-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="b2daf-127">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*GROUPING*"</span><span class="sxs-lookup"><span data-stu-id="b2daf-127">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="b2daf-128">**Política**</span><span class="sxs-lookup"><span data-stu-id="b2daf-128">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2daf-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b2daf-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2daf-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b2daf-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2daf-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2daf-131">Requirements</span></span>



| <span data-ttu-id="b2daf-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2daf-132">Requirement</span></span> | <span data-ttu-id="b2daf-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b2daf-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2daf-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2daf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b2daf-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b2daf-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2daf-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2daf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b2daf-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b2daf-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b2daf-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2daf-138">Namespace</span></span><br/>                | <span data-ttu-id="b2daf-139">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b2daf-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="b2daf-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b2daf-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2daf-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2daf-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2daf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b2daf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2daf-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2daf-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2daf-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2daf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2daf-145">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="b2daf-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

