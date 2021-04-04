---
title: Classe MDM_PassportForWork_Biometrics01
description: A \_ classe MDM PassportForWork \_ Biometrics01 define as configurações biométricas.
ms.assetid: 64012526-eac6-4f01-8665-2bd460bc1b93
keywords:
- Classe MDM_PassportForWork_Biometrics01
- Classe MDM_PassportForWork_Biometrics01, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Biometrics01
- MDM_PassportForWork_Biometrics01.InstanceID
- MDM_PassportForWork_Biometrics01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132351f17b6f242e39d6e6d6680aa756d5f7b5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085388"
---
# <a name="mdm_passportforwork_biometrics01-class"></a><span data-ttu-id="af579-105">\_ \_ Classe BIOMETRICS01 do MDM PassportForWork</span><span class="sxs-lookup"><span data-stu-id="af579-105">MDM\_PassportForWork\_Biometrics01 class</span></span>

<span data-ttu-id="af579-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="af579-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="af579-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="af579-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="af579-108">A classe **MDM \_ PassportForWork \_ Biometrics01** define as configurações biométricas.</span><span class="sxs-lookup"><span data-stu-id="af579-108">The **MDM\_PassportForWork\_Biometrics01** class defines biometric settings.</span></span>

<span data-ttu-id="af579-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="af579-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="af579-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af579-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Biometrics01
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
  boolean FacialFeaturesUseEnhancedAntiSpoofing;
};
```

## <a name="members"></a><span data-ttu-id="af579-111">Membros</span><span class="sxs-lookup"><span data-stu-id="af579-111">Members</span></span>

<span data-ttu-id="af579-112">A **classe \_ \_ Biometrics01 de MDM PassportForWork** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="af579-112">The **MDM\_PassportForWork\_Biometrics01** class has these types of members:</span></span>

-   [<span data-ttu-id="af579-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="af579-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af579-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="af579-114">Properties</span></span>

<span data-ttu-id="af579-115">A **classe \_ \_ Biometrics01 do MDM PassportForWork** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="af579-115">The **MDM\_PassportForWork\_Biometrics01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="af579-116">FacialFeaturesUseEnhancedAntiSpoofing</span><span class="sxs-lookup"><span data-stu-id="af579-116">FacialFeaturesUseEnhancedAntiSpoofing</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="af579-117">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="af579-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af579-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="af579-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="af579-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="af579-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af579-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="af579-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af579-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af579-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af579-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="af579-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="af579-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="af579-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="af579-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="af579-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af579-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="af579-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af579-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af579-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af579-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="af579-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="af579-128">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="af579-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="af579-129">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/PassportForWork/"</span><span class="sxs-lookup"><span data-stu-id="af579-129">For this class, the string is "./Vendor/MSFT/PassportForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="af579-130">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="af579-130">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="af579-131">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="af579-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af579-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="af579-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af579-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af579-133">Requirements</span></span>



| <span data-ttu-id="af579-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="af579-134">Requirement</span></span> | <span data-ttu-id="af579-135">Valor</span><span class="sxs-lookup"><span data-stu-id="af579-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af579-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af579-136">Minimum supported client</span></span><br/> | <span data-ttu-id="af579-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="af579-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af579-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af579-138">Minimum supported server</span></span><br/> | <span data-ttu-id="af579-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="af579-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="af579-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="af579-140">Namespace</span></span><br/>                | <span data-ttu-id="af579-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="af579-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="af579-142">MOF</span><span class="sxs-lookup"><span data-stu-id="af579-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af579-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af579-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="af579-144">DLL</span><span class="sxs-lookup"><span data-stu-id="af579-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af579-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af579-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af579-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="af579-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af579-147">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="af579-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

