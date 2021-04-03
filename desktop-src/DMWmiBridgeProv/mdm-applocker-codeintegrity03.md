---
title: Classe MDM_AppLocker_CodeIntegrity03
description: A \_ classe CodeIntegrity03 do MDM AppLocker \_ define a política para a integridade do código.
ms.assetid: 8e7649b4-2e89-4d79-923e-3767e5b0ea52
keywords:
- Classe MDM_AppLocker_CodeIntegrity03
- Classe MDM_AppLocker_CodeIntegrity03, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_CodeIntegrity03
- MDM_AppLocker_CodeIntegrity03.InstanceID
- MDM_AppLocker_CodeIntegrity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff702f2887f47c1cc5fcebeb4b8ec9a08c450b8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644575"
---
# <a name="mdm_applocker_codeintegrity03-class"></a><span data-ttu-id="63a3a-105">\_ \_ Classe CODEINTEGRITY03 do MDM AppLocker</span><span class="sxs-lookup"><span data-stu-id="63a3a-105">MDM\_AppLocker\_CodeIntegrity03 class</span></span>

<span data-ttu-id="63a3a-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="63a3a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="63a3a-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="63a3a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="63a3a-108">A **classe \_ \_ CodeIntegrity03 do MDM AppLocker** define a política para a integridade do código.</span><span class="sxs-lookup"><span data-stu-id="63a3a-108">The **MDM\_AppLocker\_CodeIntegrity03** class defines the policy for Code Integrity.</span></span>

<span data-ttu-id="63a3a-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="63a3a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a3a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63a3a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_CodeIntegrity03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="63a3a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="63a3a-111">Members</span></span>

<span data-ttu-id="63a3a-112">A **classe \_ \_ CodeIntegrity03 do MDM AppLocker** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="63a3a-112">The **MDM\_AppLocker\_CodeIntegrity03** class has these types of members:</span></span>

-   [<span data-ttu-id="63a3a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63a3a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63a3a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63a3a-114">Properties</span></span>

<span data-ttu-id="63a3a-115">A **classe \_ \_ CodeIntegrity03 do MDM AppLocker** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="63a3a-115">The **MDM\_AppLocker\_CodeIntegrity03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63a3a-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="63a3a-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a3a-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63a3a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a3a-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63a3a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a3a-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63a3a-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63a3a-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="63a3a-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="63a3a-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="63a3a-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a3a-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63a3a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a3a-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63a3a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63a3a-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63a3a-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63a3a-125">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="63a3a-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="63a3a-126">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span><span class="sxs-lookup"><span data-stu-id="63a3a-126">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="63a3a-127">**Política**</span><span class="sxs-lookup"><span data-stu-id="63a3a-127">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63a3a-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63a3a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63a3a-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="63a3a-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="63a3a-130">Qualificadores: **octetstring**</span><span class="sxs-lookup"><span data-stu-id="63a3a-130">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63a3a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63a3a-131">Requirements</span></span>



| <span data-ttu-id="63a3a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="63a3a-132">Requirement</span></span> | <span data-ttu-id="63a3a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="63a3a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a3a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63a3a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="63a3a-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="63a3a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63a3a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63a3a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="63a3a-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="63a3a-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="63a3a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="63a3a-138">Namespace</span></span><br/>                | <span data-ttu-id="63a3a-139">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="63a3a-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="63a3a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="63a3a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63a3a-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63a3a-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="63a3a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="63a3a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63a3a-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63a3a-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a3a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="63a3a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a3a-145">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="63a3a-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

